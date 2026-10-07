# Praktisk verktygsuppgift

Det här projektet hör till kursen **Introduktion till modern utvecklarroll**
på utbildningen Mjukvaruutvecklare med AI-inriktning, MAI26 Malmö.

Övningen går ut på att skapa och hitta filer med Bash, öppna projektet i
VS Code och dokumentera arbetet med Markdown. Git används för att spara
ändringar som tydliga versioner, och GitHub används för att dela projektet.

## Projektets innehåll

`mina-bash-kommandon.txt` beskriver terminalkommandon och förklarar filer,
mappar och sökvägar. Den här README-filen beskriver övningen, Git-kommandon
och centrala begrepp.

## Git-kommandon

- `git init` skapar ett lokalt Git-repository i projektmappen. Git sparar
  sin information i den dolda mappen `.git`.
- `git status` visar vilka filer som är nya eller ändrade och vilka ändringar
  som har valts till nästa commit. `git status --short` visar en kortare lista.
- `git add mina-bash-kommandon.txt` väljer ändringarna i den filen till nästa
  commit. Samma kommando används med de andra filernas namn när de ändras.
- `git commit -m "Beskriv ändringen"` sparar de valda ändringarna som en lokal
  version. Meddelandet förklarar vad som ändrades.
- `git log --oneline` visar en kort rad för varje commit. Med `--reverse`
  visas den äldsta först, så att arbetsgången går att följa i ordning.
- `git branch -M main` ger den aktuella branchen namnet `main`.
- `git remote add origin https://github.com/aliteex55-bit/mai26ma-praktisk-verktygsuppgift.git`
  kopplar det lokala projektet till GitHub-repositoryt. `origin` är ett lokalt
  kortnamn för den adressen.
- `git remote -v` visar vilka adresser som är kopplade till projektet.
- `git push -u origin main` skickar lokala commits på `main` till GitHub och
  kopplar branchen till `origin/main`. Efter det räcker normalt `git push`.
- `git pull --ff-only` hämtar ändringar från det anslutna fjärrrepositoryt och
  uppdaterar den lokala branchen om det går utan att slå ihop två olika
  utvecklingsspår. Om historiken har gått åt olika håll avbryts kommandot.
  Vanlig `git pull` hämtar och integrerar fjärrändringar enligt Git-inställningarna.
- `git diff` visar ändringar som ännu inte har lagts till med `git add`.
  `git diff --cached` visar de ändringar som har valts till nästa commit.
- `git config user.name` och `git config user.email` ställer in författarens
  namn och e-post när ett värde anges efter kommandot. Utan `--global` gäller
  inställningen bara detta repository. Här används GitHubs noreply-adress.

`git add` och `git commit` arbetar lokalt. En commit skickas till GitHub först
med `git push`. `git pull` går åt andra hållet: från fjärrrepositoryt till
det lokala projektet.

## Repository, commit och versionshistorik

Ett **repository**, ofta förkortat repo, är ett projekt vars filer och
ändringshistorik hanteras av Git. Det finns lokalt på datorn och kan också
finnas som ett fjärrrepository på GitHub, så att andra kan ta del av arbetet.

En **commit** är en sparad version av de ändringar som valts med `git add`.
Den har ett eget id och ett meddelande som beskriver ändringen. En commit
kan till exempel lägga till förklaringarna av Git-kommandon i README.

**Versionshistoriken** är följden av commits. Den visar hur projektet har
utvecklats, vilka ändringar som hör ihop och när de sparades. Historiken
går att läsa med `git log` och kan användas för att jämföra versioner eller
hitta när ett fel infördes.

Små commits med tydliga meddelanden gör historiken lättare att förstå.
Därför sparas kommandodokumentationen, README-beskrivningen,
Git-kommandona och begreppsförklaringarna som separata ändringar.
