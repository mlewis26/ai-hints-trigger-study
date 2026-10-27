# The Tri: Build Documentation

**Documented:** October 27, 2026, before B1 begins (November 5, 2026), as stated in PREREGISTRATION.md.

The Tri is a small physical cue. Tapping it with my iPhone switches Claude into hints-only mode on my Mac. Tapping it again switches hints mode off.

## 1. The physical object

| Part | Details |
|---|---|
| Material | UV resin, hard type, clear |
| Mold | Pyramid-shaped silicone mold |
| Size | 3.5 cm base length, 2.7 cm tall |
| Curing | UV lamp, 10 minutes |
| Tag | NFC sticker attached to the bottom of the pyramid |
| Finished | October 24, 2026 |

## 2. What a tap does

**First tap (hints on):**

1. The iPhone reads the NFC tag.
2. An iPhone Shortcuts automation turns on a Focus mode called **Hints**.
3. The same automation connects to my Mac over the home Wi-Fi and runs a Mac shortcut called **Tri Hints**.
4. **Tri Hints** brings the Claude app to the front, then types and sends the message **"hints mode on"** in the open conversation.
5. A saved instruction in my Claude settings tells Claude what "hints mode on" means (section 5).

**Second tap (hints off):**

1. The automation sees that the Hints Focus is already on, so it turns Hints off.
2. It runs a Mac shortcut called **Tri Off**, which sends **"hints mode off"** in the open conversation.

## 3. iPhone automation

Built in the Shortcuts app: **Automation → NFC → "Tri" is scanned**, set to run immediately, without asking first.

```
Get Current Focus
If Current Focus has any value
    Set Focus: Turn Hints Off
    Run Script Over SSH: shortcuts run "Tri Off"
Otherwise
    Set Focus: Turn Hints On until Turned Off
    Run Script Over SSH: shortcuts run "Tri Hints"
End If
```

Run Script Over SSH connects to the Mac on the local network (port 22) using Remote Login.

## 4. Mac shortcuts

Both are in the Mac Shortcuts app, each with one **Run AppleScript** action.

**Tri Hints**

```applescript
on run {input, parameters}
	tell application "Claude" to activate
	delay 1.5
	tell application "System Events"
		keystroke "hints mode on"
		delay 0.3
		key code 36
	end tell
	return input
end run
```

**Tri Off** is the same script, but it types `"hints mode off"`.

**Mac settings needed:**
- **macOS 27.** It was updated from 15.5 on October 24 while building this. The Mac automation tab didn't let me create a Focus automation, so the iPhone triggers the Mac over SSH instead.
- **Remote Login** turned on (System Settings → General → Sharing), limited to my user account.
- **Accessibility** permission for Shortcuts and sshd-keygen-wrapper (System Settings → Privacy & Security → Accessibility), so the shortcut can type into Claude.
- **Allow Running Scripts** turned on in Shortcuts settings.
- The Mac must be awake and on the same Wi-Fi as the iPhone.

## 5. What "hints mode on" means

Saved in Claude under **Settings → Profile → personal preferences**. It applies only when the message is sent:

> When I send "hints mode on", switch to hints-only for the rest of that topic:
> - Never give me the full answer or finished code. Give one hint at a time, starting small: a guiding question, which concept or pattern applies, or where my mistake is.
> - Only explain directly if it's a concept I've genuinely never learned. Then teach the concept, but still let me write the solution myself.
> - If I ask for the answer, remind me I'm in hints mode and give a bigger hint instead.
> - Keep replies short and plain, one step at a time.
> - At the end of the topic, remind me to log the row (Hints mode = Yes, and Outcome: Me, AI, or Mixed).
>
> When I send "hints mode off", go back to normal for the rest of the conversation.

## 6. Testing

Tested on October 24, 2026, with repeated on/off taps. Each first tap sent "hints mode on" and each second tap sent "hints mode off" in the Claude conversation. The test messages weren't learning sessions and weren't logged as study data. The Tri was put away for the rest of A1.

## 7. Use during the study

- **B phases (Nov 5–18 and Dec 3–16):** the Tri is out. I tap it at the start of a topic to turn hints mode on, and tap again to turn it off.
- **A phases (Oct 23–Nov 4 and Nov 19–Dec 2):** the Tri is put away, and I use Claude normally.
- Scope stays the same as the preregistration: Claude, in one ongoing conversation, used mainly on my Mac. The iPhone only reads the tap.
