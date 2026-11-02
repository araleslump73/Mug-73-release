[English](README.md) · **Italiano**

# Mug-73

Sintetizzatore monofonico in stile anni '70 (con modo polifonico opzionale): tre oscillatori, filtro ladder a 24 dB/ottava, due inviluppi, LFO, arpeggiatore, step sequencer, catena di effetti completa e ingresso audio esterno. Funziona come **plugin CLAP** nel tuo DAW e come **app standalone** su Windows, macOS e Linux.

**[Scarica l'ultima versione](../../releases/latest)**

[☕ Sostieni Mug-73 su Ko-fi](https://ko-fi.com/mat73)

> Il codice sorgente non è pubblicato. Questa repo contiene i download, la documentazione e le segnalazioni.

## Cosa c'è dentro

- **Voce**: 3 oscillatori (6 forme d'onda, 6 registri), rumore (bianco/rosa), mixer con overload, filtro ladder a 4 poli con enfasi e contour, due inviluppi ADSR, LFO (libero o a tempo) con cinque destinazioni. Mono o poly (2–8 voci).
- **Canale EXT**: voce, chitarra o una traccia qualsiasi entra nel mixer come un oscillatore e passa dal filtro e dall'inviluppo (a gate o drone). Nel DAW usa un ingresso sidechain; nello standalone scegli l'ingresso audio nelle Settings.
- **Arpeggiatore e sequencer a 16 passi** che seguono tempo e transport del DAW.
- **Effetti**: drive, compressore, EQ a 3 bande, phaser/flanger, chorus, rotary, delay (mono/ping-pong), riverbero.
- **170 preset di fabbrica** in 12 gruppi; salvi i tuoi, modifichi il file a mano, esporti e importi.
- **MIDI**: pitch bend, mod wheel, program change, MIDI Learn su ogni controllo.
- Leggerissimo per la CPU (circa 2–3% di un core con tutti gli effetti), quindi vanno bene i buffer piccoli.

## Installazione

1. Scarica da **Releases** lo zip per il tuo sistema e decomprimilo.
2. Copia `Mug-73.clap`:
   - **Windows**: `C:\Program Files\Common Files\CLAP\`
   - **macOS**: `~/Library/Audio/Plug-Ins/CLAP/`, poi `xattr -dr com.apple.quarantine ~/Library/Audio/Plug-Ins/CLAP/Mug-73.clap` (i file non sono firmati)
   - **Linux**: `~/.clap/`
3. Riscansiona i plugin nel DAW: **Mug-73** compare tra gli strumenti.

I file non sono firmati digitalmente, quindi Windows SmartScreen può avvisarti la prima volta.

Per la latenza più bassa su Windows usa nel DAW il driver ASIO della tua scheda audio con buffer di 64–256 campioni.

> Il **VST3** non c'è: le librerie VST3 disponibili per questo framework sono GPLv3, incompatibili con una distribuzione senza sorgente. Usa la versione CLAP (supportata da Bitwig, REAPER, FL Studio, Studio One, MultitrackStudio e altri) o l'app standalone.

## App standalone

Avvia `Mug-73` (`Mug-73.exe` su Windows). Suona sull'uscita audio di sistema e collega la prima tastiera MIDI che trova. Puoi suonare anche con la tastiera a schermo o quella del PC (A W S E D F T G Y H U J K O L P; Z/X cambiano ottava; Spazio avvia il sequencer).

```
Mug-73 --midi-input ""         elenca gli ingressi MIDI
Mug-73 --midi-input "nome"     usa quell'ingresso
Mug-73 --output-device ""      elenca le uscite audio
Mug-73 --period-size 128       buffer in campioni
Mug-73 --help                  tutte le opzioni
```

Le Settings (livello uscita, uscita audio, **ingresso audio per EXT**, buffer, ingresso MIDI, dimensione dell'interfaccia) si salvano e si applicano riavviando l'app. L'ingresso audio all'inizio è spento perché un microfono aperto non inneschi un fischio: usa le cuffie.

## Segnalazioni

Bug e richieste: apri una [issue](../../issues), indicando sistema, DAW e versione del plugin.

## Sostegno

Mug-73 è gratuito. Se ti è utile, puoi sostenerne lo sviluppo con una mancia su [Ko-fi](https://ko-fi.com/mat73). Grazie!

## Licenza

Uso gratuito, anche per la musica che pubblichi o vendi; vietata la ridistribuzione. Vedi [LICENSE.txt](LICENSE.txt). Componenti di terze parti: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
