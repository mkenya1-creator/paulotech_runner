# PauloTech Runner

Endless runner game iliyojengwa kwa Flutter + Flame, tayari kwa mchakato wako wa kawaida:
**GitHub → CodeMagic → APK** (bila kompyuta).

## Hali ya sasa

Mchezo tayari unafanya kazi kikamilifu na mhusika wa "placeholder" (sanduku la zambarau lenye jicho na neno "WEWE").
Unaweza kuu-build na kuu-test sasa hivi, kisha ubadilishe sanamu baadaye — hakuna haja ya kusubiri sprite kabla ya kutest logic.

## Jinsi mchezo unavyofanya kazi

- Gusa skrini kuruka (jump)
- Vikwazo (mistatili nyekundu) vinakuja kutoka kulia
- Ukigonga kizuizi → Game Over, alama zinaonyeshwa
- Gusa tena kuanza upya
- Kasi inaongezeka pole pole kadri alama zinavyoongezeka

## Namna ya kuongeza mhusika wako (sprite)

Faili za picha zinatakiwa ziwe hapa: `assets/images/`

Zihitajika (PNG, background wazi/transparent):
1. `player_idle.png` — umesimama
2. `player_run1.png` — mguu mmoja mbele
3. `player_run2.png` — mguu mwingine mbele
4. `player_jump.png` — akiwa hewani

**Hatua za kutengeneza:**
1. Piga picha yako mkao unaotakiwa, background rangi moja rahisi
2. Tumia app ya "remove background" (mfano Remove.bg app ya simu) — inakupa PNG yenye transparency
3. (Hiari) Tumia app ya cartoon/anime filter ili ionekane kama mchoro wa mchezo, si picha halisi
4. Weka faili hizo 4 kwenye `assets/images/` kwa majina hayo hasa

Mchezo utaziona kiotomatiki wakati wa `onLoad()` — ukikosa faili, placeholder itaendelea kuonekana (haita-crash).

## Kujenga APK (utaratibu wako wa kawaida)

1. Fungua GitHub app kwenye simu, tengeneza repo mpya, pakia hizi faili zote
2. Unganisha repo hiyo na CodeMagic
3. Codemagic itasoma `codemagic.yaml` iliyopo hapa — badilisha email ya `recipients` kwenye faili hiyo kabla ya build ya kwanza
4. Bonyeza "Start new build" → workflow `android-apk`
5. Baada ya kukamilika, APK itatumwa kwenye email yako au unaweza kuipakua moja kwa moja kutoka CodeMagic

## Maboresho yanayofuata (hiari)

- Ongeza sauti (jump sound, collision sound) kupitia `flame_audio` — tayari imewekwa kwenye `pubspec.yaml`
- Ongeza coins za kukusanya badala ya/pamoja na alama za umbali
- Ongeza background ya Tanzania (picha ya mtaa) badala ya rangi tambarare
- Ongeza high score inayohifadhiwa kwenye simu (SharedPreferences)
- Badilisha "vikwazo" viwe na maumbo tofauti (mawe, mashimo, ndege)

Ukitaka nyongeza yoyote kati ya hizi, niambie tu.
