# Fråga 1: Versionshantering vs vanliga filer

## För Godkänt (G): Vad är versionshantering och vad är den stora skillnaden mellan att spara en fil via editorns vanliga sparaknapp och att spara ändringar i Git?

**SVAR:**

- Versionshantering är ett system som sparar hela historiken över ett projekt. Så man kan se vad som har ändrats, när det har ändrats och varför. Man kan gå tillbaka till tidigare versioner och enkelt sammarbeta med andra.

- Sparaknappen i editorn skriver enbart över filen på datorns disk. Medans att spara ändringar i git tar en permanent ögonblicksbild som du själv väljer ut och kan förse med ett meddelande.

## För Väl Godkänt (VG): Förklara vad som menas med att Git sparar en tidslinje av frysta ögonblicksbilder (commits). Vad bevisar det faktum att du när som helst kan klicka på din allra första commit på GitHub och fortfarande se alla tre TODO kvar i koden, trots att filen på din dator ser helt annorlunda ut idag?

**SVAR:**

- Git sparar projeket som en tidslinje av commits. Varje commit är som en frusen ögonblicksbild av alla filer vid ett visst tillfälle. Nya ändringar läggs till som nya commits ovanpå de gamla i stället för att skriva över dem.

- Det bevisar att historiken förblir orörd. Den gamla versionen finns kvar oförändrad trots att den nuvarande filen på min dator ser annorlunda ut.

# Fråga 2: Arbetsytan, Staging och Commits

## För Godkänt (G): Beskriv vad kommandona git status, git add och git commit gör i det dagliga arbetsflödet och när du kör dem.

**SVAR:**

- git status: Visar vilka filer som är ändrade, nya filer eller filer som redan är förberädda för commit.

- git add: Flyttar ändringar i filer från arbetsytan till "staging".

- git commit: Sparar de utvalda ändringarna permanent i historken tillsammans med ett meddelande.

## För Väl Godkänt (VG): Förklara relationen mellan arbetsytan (arket på skrivbordet), staging (kuvertet) och commit (arkivlådan). Förklara också varför Git protesterar med no changes added to commit om man har ändrat filen i editorn och försöker köra git commit direkt utan git add.

**SVAR:**

- Arbetsytan är arket på skrivbordet där jag redigerar mina filer, staging är kuvertet där jag lägger dem ändringar jag vill skicka med och commit är som arkivlådan där kuvertet med arket sparas permanent.

- Git protesterar eftersom ändringen fortfarande bara ligger på skrivbordet ("arket"). Kuvertet är alltså tomt då och Git har inget utvalt att lägga i arkivlådan.

# Fråga 3: Lådan hemma vs Montern på GitHub

## För Godkänt (G): Vad är skillnaden mellan mappen på din dator och repot på GitHub, och vad gör kommandot git push?

**SVAR:**

- Mappen på min dator är mitt lokala repo, filerna jag arbetar med och sparar commits. Repot på GitHub är en kopia som ligger online som andra kan se och ta del av.

- git push: Skickar mina commits från det lokala repot upp till GitHub online.

## För Väl Godkänt (VG): Förklara konceptet med de två rummen / minnesytorna (lådan hemma på datorn vs glasmontern på GitHub). Förklara varför git push svarar Everything up-to-date om du har ändrat i koden men glömt att staga och committa innan du kör push.

**SVAR:**

- Det finns två separata ytor, lådan hemma där jag jobbar och sparar mina commits. Och glasmontern på GitHub där det jag skickat upp visas för andra som har tillgång till online repot. De hör ihop men är helt åtskilda, inget når glasmontern fören jag skickat det med git push.

- Git push skickar bara färdiga commits, inte ändringar som ligger på arbetsytan. Om jag har ändrat koden men glömt git add/ git commit finns det alltså inga nya commits att skicka och Git svarar med att allt är up-to-date.
