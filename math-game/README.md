# Math game — Block Math Escape

Multiplication 0–10 for ages 5–8, in a Minecraft-flavoured escape game: answer
correctly to craft a weapon out of blocks, beat the guard, and get out of the
room. Four difficulties, four skins, English and Czech, and a timed bonus round
between rooms.

Source lives in a private repository; only builds are published here.

## Which file do I want?

| File | Size | For |
|---|---|---|
| `BlockMathEscape-<version>.html` | ~150 KB | **Start here.** The whole game in one file — double-click and it opens in any browser. No install, no admin rights, works on Windows, Mac, Chromebook and tablets, works offline. |
| `BlockMathEscape-<version>-setup.exe` | ~95 MB | Windows installer. Adds a Start-menu and desktop shortcut, installs per-user so it needs no admin password. |
| `BlockMathEscape-<version>-portable.exe` | ~95 MB | Windows, no install at all — one file, run it from anywhere, including a USB stick. |

The two `.exe` files are the same game as the HTML one, wrapped in Electron so
it gets its own window and desktop icon. If you are deciding for a classroom,
the HTML file is almost always the better answer: nothing to install, nothing
for antivirus to object to, and it runs on whatever hardware the room has.

## Running the Windows build the first time

The build is not code-signed, so Windows shows:

> **Windows protected your PC** — Microsoft Defender SmartScreen prevented an
> unrecognised app from starting.

Click **More info**, then **Run anyway**. This appears once per machine. It
means “nobody paid for a certificate”, not “this is dangerous”.

Some school and corporate networks block `.exe` downloads outright. If that
happens, use the HTML file — it is not blocked anywhere and needs no permission
to run.

## Verifying a download

Every release lists a SHA-256 for each file. To check one on Windows:

```powershell
Get-FileHash .\BlockMathEscape-0.1.0-setup.exe -Algorithm SHA256
```

macOS or Linux:

```bash
shasum -a 256 BlockMathEscape-0.1.0-setup.exe
```

## Playing it

Pick a difficulty on the title screen:

| | Hearts | Rules |
|---|---|---|
| **Easy** | 8 | Pets instead of weapons; a wrong answer just costs a heart |
| **Normal** | 5 | A wrong answer must be corrected before moving on — the correction itself is free |
| **Hard** | 3 | Same correction rule, tougher kit, missions instead of the treasure hunt |
| **Sudden Death** | 1 | 100% accuracy to craft anything; bonus round is 10 questions in 20 seconds |

**MY NUMBERS** on the title screen shows which times tables the child actually
knows, and which keep coming back.
