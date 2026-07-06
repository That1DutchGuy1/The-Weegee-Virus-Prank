<p><strong><font size="6">🧟 Weegee Virus (harmless prank, I swear) — by That1DutchGuy</font></strong></p>

---

> Inspirational quote: "OBEY WEEGEE! DESTROY MARIO!."

---

<img src="./Weegee Virus Prank App/Mega_Weegee.png" alt="That One Dutch Guy" width="150" />

---

<p><strong><font size="5">⚠️ WHAT THE HELL IS THIS?</font></strong></p>

It's Weegee. He's here. He's not leaving until you make him. That's it, that's the app. 😁

---

<p><strong><font size="4">📦 Install</font></strong></p>

```
sudo dpkg -i weegee-virus_1.1.1.deb
sudo apt-get install -f   # only needed if apt whines about missing deps like a little baby
```

---

<p><strong><font size="4">▶️ Run</font></strong></p>

Open **"Weegee Virus"** from the Cinnamon menu, or pin it to the panel like the proud degenerate you are. <br>
The icon is `Weegee-Head-Front.png`. You already know what that looks like. 😌

---

<p><strong><font size="4">😈 While It's Running</font></strong></p>

* Your wallpaper gets yeeted and replaced with `Weegee-Wallpaper.png` 🖼️
* EVERY. SINGLE. DESKTOP ICON. becomes Weegee's face. I built a temporary icon theme by walking your *entire* active icon theme's inheritance chain (your theme, everything it inherits from, and hicolor as the universal fallback) and overwriting every icon file it can find. Fabulous. 🦄
  * (Photo thumbnails on your desktop are previews, not icon-theme icons, so those'll still show as themselves — that's just normal desktop behavior, not a bug, don't @ me)
* Your mouse cursor? Also Weegee now. Same trick — I generate a temporary Xcursor theme via `xcursorgen` covering every common pointer shape (arrow, text I-beam, resize handles, wait spinner, the works), inheriting from your original theme for anything I didn't explicitly cover 🖱️
* Weegee glides across your screen, above ALL your windows, click-through (so yes you can still interact with whatever's underneath him, I'm not a complete monster), swinging back and forth like a deranged pendulum forever ⏰
* The jumpscare sound (`obey-weegee-destroy-mario.mp3`) loops continuously at FULL volume, no mercy 🔊
* `Theme.mp3` loops independently too, at 50% volume, because I have SOME restraint 🎵
* Both play via GStreamer, and if your system can't decode mp3 through GStreamer they fall back to `mpg123` (still respecting that 50% volume on Theme.mp3, don't worry)

---

<p><strong><font size="4">🏳️ Making It Stop</font></strong></p>

A little Weegee-head icon shows up in your panel/tray. Click it (or right-click, I don't judge) and hit **"Restore desktop & quit"** to banish him instantly — wallpaper, icon theme, cursor theme, and both sounds all revert/stop, Mega Weegee vanishes, and the temporary icon/cursor folders get deleted like they never existed. 🙏🏻

Launching the shortcut a second time while it's already running ALSO banishes him — it's a toggle, motherfucker! 🔁

---

<p><strong><font size="4">🗑️ Uninstall</font></strong></p>

```
sudo apt remove weegee-virus
```

---

<p><strong><font size="3">📝 Notes (the boring but important shit)</font></strong></p>

* Only EVER runs when *you* open it. No autostart, no background service, no persistence. I'm evil, not a war criminal. 😇
* Cursor swapping needs `xcursorgen`, bundled inside `x11-apps` (pulled in automatically as a dependency). If it's somehow missing, the app just skips the cursor swap instead of exploding. 💥
* Sound needs GStreamer plugins (`gstreamer1.0-plugins-good`, and `-ugly` for mp3 decoding), pulled in as dependencies/recommends. Still no mp3 decoding? `mpg123 --loop` has your back.
* Tested against the GTK/Cinnamon APIs used in Linux Mint 22 (Cinnamon Edition), because that's what The Cinnamon XP Meme Machine runs. The icon-theme cloning step reads whatever icon theme you currently have active, so it adapts to your setup automatically. 🐧

---

<p><strong><font size="3">💬 Q & A</font></strong></p>

> **Q: Is this actually a virus?**  <br>
> **A:** No, you absolute drama queen. It's a prank app with an on/off switch and zero persistence. Read the notes above, you dumbass. 🤦🏻‍♂️

> **Q: Will this break my desktop?**  <br>
> **A:** Nah. Everything it touches, it can put back exactly the way it found it. Click the tray icon, Weegee goes away, life resumes. 👍🏻

> **Q: Why does the cursor/icon swap work by "walking the inheritance chain"?**  <br>
> **A:** Because your icon theme almost never has every icon defined itself — it inherits from parent themes, which inherit from hicolor. If I only touched your theme's own files, half your icons would stay normal and ruin the bit. Can't have that. 🎭

> **Q: Can I make it louder?**  <br>
> **A:** The jumpscare's already at full volume, my dude. That IS the loudest. 🔊

> **Q: Is the code AI generated?**  <br>
> **A:** Partially. I use AI tools to help debug and brainstorm when I'm stuck, but I meticulously verify every snippet before it goes anywhere near this repo. Don't judge me. 🤷🏻‍♂️

---
