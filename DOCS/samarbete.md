# Samarbete i ett gemensamt repository

Ett gemensamt repository samlar ett utvecklingsteams kod, dokumentation
och ändringshistorik. Alla kan utgå från samma projekt och se vad som har
ändrats. Varje person arbetar i en lokal kopia och delar sina commits
genom att skicka dem till det gemensamma fjärrrepositoryt, exempelvis på GitHub.

## Exempel på arbetsflöde i ett team

1. En ny teammedlem klonar repositoryt med `git clone` och får en lokal
   kopia av projektet och dess historik.
2. Innan ett nytt arbete börjar hämtas aktuella ändringar med `git pull`.
   En egen branch gör det möjligt att arbeta med en avgränsad uppgift.
3. Personen ändrar relevanta filer och kontrollerar resultatet med
   `git status` och `git diff`.
4. Ändringarna väljs med `git add` och sparas med `git commit`. Ett tydligt
   commit-meddelande hjälper andra att förstå ändringen.
5. Med `git push` skickas commits till GitHub. En pull request kan sedan
   användas för att be en kollega granska ändringarna innan de slås ihop
   med huvudbranchen.
6. När ändringarna har slagits ihop kan resten av teamet hämta dem.

Det här är ett exempel på hur ett team kan arbeta. I denna övning räcker
det att dokumentera samarbetet och publicera filerna; någon gemensam
kodgranskning eller pull request behöver inte genomföras.

## Varför historik och kommunikation behövs

Historiken gör det möjligt att se vem som sparade en ändring, läsa varför
den gjordes och jämföra olika versioner. Små commits och tydliga meddelanden
underlättar både granskning och felsökning.

Om två personer ändrar samma del av en fil kan en konflikt uppstå.
Då behöver de jämföra ändringarna, komma överens om rätt innehåll och
kontrollera resultatet innan det sparas och delas igen. Git hjälper till
att upptäcka konflikten, men teamet måste avgöra hur den ska lösas.

Ett publikt repository kan läsas av andra. Rätten att skriva till projektet
styrs däremot av behörigheter; att kunna läsa ett repo innebär inte att
vem som helst kan ändra huvudbranchen.
