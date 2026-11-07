# SiUI Gaming — installer e aggiornamenti

Qui escono gli **installer firmati** di [SiUI Gaming](https://github.com/Zaruka96/SiUI-Gaming), l'aggregatore di librerie di gioco per Windows. Il codice sorgente sta nel repository privato: qui ci sono solo i binari, perché un'applicazione installata non ha un token con cui scaricarli da un repository chiuso.

## Scaricare

Vai in **[Releases](../../releases/latest)** e prendi `SiUI.Gaming_<versione>_x64-setup.exe`.

Chi ha già SiUI installata non deve fare niente: l'applicazione vede da sola la versione nuova, la scarica e si riavvia aggiornata.

## I file di ogni rilascio

| File | Cos'è |
|---|---|
| `SiUI.Gaming_<v>_x64-setup.exe` | L'installer, quello da scaricare |
| `SiUI.Gaming_<v>_x64_en-US.msi` | Lo stesso pacchetto in formato MSI, per chi distribuisce |
| `*.sig` | La firma di ciascun pacchetto |
| `latest.json` | Il file che l'applicazione legge per sapere se c'è una versione nuova |

Ogni pacchetto è firmato con una chiave privata che non lascia mai la build. L'applicazione porta con sé la chiave pubblica e verifica la firma **prima** di installare: un pacchetto non firmato, o firmato con un'altra chiave, viene rifiutato.
