# Arcana pack

The files the Arcana Prism instance downloads before every launch. Built by `tools/pack.py` in the
Arcana repository and replaced whole on every patch; nothing here is edited by hand.

**Playing:** download `Arcana.zip` from the latest release, then in Prism Launcher choose
Add Instance > Import and pick it. Launch. It keeps itself up to date from here.

**If the game crashes and the crash report names the C2 compiler** (`hs_err_pid….log`, "C2 CompilerThread",
seen on Java 25.0.1 with Distant Horizons on): it is a bug in that Java build, not in the game.
1. Newer Java, the real fix. In Prism, Edit the Arcana instance > Settings > Java, tick the Java installation box,
   press Download Java, choose the newest Java 25 (Temurin or Zulu) and select it. Launch.
2. If you cannot change Java: in the same page tick JVM arguments and add `-XX:TieredStopAtLevel=1`. It turns off
   the JIT's optimising compiler, which is where the crash lives; the game stays correct and costs a little frame
   time. Remove it after updating Java.
3. Or turn Distant Horizons off (it is an optional mod; Prism's mod list).
