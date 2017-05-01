Hvor mange kjenner til versjonskontroll generelt?

Hvor mange har vært borti Git, spesielt?

Hvor mange av dere bruker Git jevnlig, på skole eller jobb?

Denne talken er for dere. Dere andre som ikke kan Git eller versjonskontroll: Google it, kjør en tutorial og lær deg det. Det er en av de smartete tingene du kan gjøre, du vil komme til å trenge det før eller senere uansett.



De fleste av oss bruker basics, add, commit, push, pull til daglig. Sikkert også branch og merge hvis man jobber sammen med andre.

Men det finnes en del andre morsomme ting i git-verktøykassa som kan være kult å kjenne til.

Vise dere en håndfull. Her er poenget bare å fortelle dere litt om hva som finnes, ikke lære dere detaljene i hvordan man gjør det. Hvis dere vil sjekke mer har jeg en lenke på slutten til ressurser dere kan lese.


1: Log-alias

Først en liten sak. Default output fra git log ser slik ut: Ikke spesielt lesbar eller kompakt, litt vanskelig å få oversikt.
Log-kommandoen tar mange opsjoner, og folk på nettet har funnet ut at den kommandoen her gir mye nicere output.
I stedet for å huske på den kan du legge til et alias i gitconfigen din, slik at du bare kan skrive git ls i stedet.

2: commit --amend
Triks 2:

Det hender ofte man glemmer en liten ting man egentlig ville ha med på den siste committen man gjorde. Det er litt teit å gjøre en ny commit da, men det løser vi fint med en commit --amend. Da smelter den bare inn i forrige commit, og du kan redigere meldingen hvis du vil også. Bare pass på å ikke gjøre det hvis du har pusha committen din allerde, hvis du vil pushe den amendede commiten da, må du nemlig gjøre en såkalt force push.

3: Force push
Det bringer meg elegant over på tips 3: Force push. Og her er tipset: Ikke gjør det (med mindre du vet hva du gjør). Det skaper trøbbel og kaos for de andre på teamet. Force-push dukker som regel opp i forbindelse med amend og andre former for "endring" av commits du har gjort.

4: Interaktiv rebase

Som bringer meg elegant videre på neste tema, nemlig interaktiv rebase. Med det verktøyet kan jeg få opp en liste over alle commits jeg har gjort, og slette, omrokkere og slå sammen commits. Ganske fett! <bruk en serie screenshots her, men commits ala "whops", "fuckit", "fikser commit for tre commits siden", etc>.

5: Bisect?

6: Til slutt: Noen av dere har kanskje lagt merke til at jeg har  branchnavn i terminalen og kryss-merke for om jeg har lokale endringer som ikke er committet. Jeg bruker Zsh med oh-my-zsh, men dette finnes også for dere som bruker bash.

Alt jeg har fortalt om ligger på github.com/fredva/git-triks. Når jeg har sagt at noe er smart eller ikke smart, nyttig eller ikke nyttig, er det helt sikkert mange på internett som er uenig, så bottom line er: Google, les og lær og gjør det opp en egen mening om hvilke verktøy du synes er nyttige og fornuftige å bruke.

Er det noen som lurer på noe, så kom bort og snakk med meg etterpå da vel. Det beste jeg vet er å diskutere Git og drikke øl.
