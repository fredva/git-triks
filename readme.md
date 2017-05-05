# Noen git-triks

Dette notatet er et sammendrag av en lyntale jeg holdt på IFI 10. mai 2017. Du kan laste ned slidene i [Keynote](Slides.key)- eller [PDF](Slides.pdf)-format.

## 1. Log-alias og annen config

Min `.gitconfig` ligger i [dotfiles-repoet mitt](https://github.com/fredva/dotfiles/blob/master/gitconfig) her på GitHub. Der ligger `git ls` og `git lg`-aliasene jeg viste i lyntalen, samt en del andre nyttige alias og config.

### Diff so fancy

Jeg bruker [Diff so fancy](https://github.com/so-fancy/diff-so-fancy) for å vise mer fancy differ med `git diff`. Sjekk det ut på GitHub for installasjon (Mac: `brew install diff-so-fancy`) og legg til [dette](https://github.com/fredva/dotfiles/blob/master/gitconfig#L30-L32) i `.gitconfig`, så er du good to go.

## 2. Amende commits

Du skriver `git commit --amend` for å smelte endringene dine inn i forrige commit. Du kan oppgi en ny commitmelding med `git commit --amend -m "<melding>"` om du vil, hvis ikke brukes meldingen fra tidligere.

Se for øvrig:

- [Dokumentasjonen til `git-commit`](https://git-scm.com/docs/git-commit)
- [Kapittel 7.6 om "Rewriting History" i boka Pro Git](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History)

## 3. Force push

Kortversjonen her er: Vær svært forsiktig med bruk av `git push --force`. Kjapp Googling på _"git push force"_ gir deg masse lesestoff om hvorfor det er farlig, og hva man kan gjøre for å unngå katastrofer.

Atlassian har skrevet [en god bloggpost](https://developer.atlassian.com/blog/2015/04/force-with-lease/) om `git push --force-with-lease`, et litt tryggere alternativ til `git push --force`.

## 4. Interaktiv rebase

["Rewriting History" i Pro Git](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History), som jeg lenket til under [Amend](#2-amende-commits), har også en god intro til interaktiv rebasing.

Se for øvrig [min lyntale om rebase fra JavaZone 2016](https://vimeo.com/182068915).

## 5. Fet prompt

Jeg bruker shellet [`zsh`](http://www.zsh.org/) med pluginen [Oh My Zsh](http://ohmyz.sh/) for å få en fancy git-aware prompt. Default theme til Oh my zsh støtter dette, men det finnes også mange andre fancy themes med varierende grad av git-støtte.

Google _"git prompt bash"_ for å se hvordan du setter opp lignende prompt i bash.

## Andre tips

Her er noen tips jeg ikke rakk å dekke i lyntalen.

### Sjekk ut forrige branch

Et lite triks er å bruke `git checkout -` for å bytte tilbake til branchen du var på sist. Visste du at `cd -` gjør det samme i terminalen, altså bytter tilbake til forrige katalog? Se, der lærte du to ting!

### Patch add

Bruk `git add -p` for å kun legge til deler av filer. Detaljer finner du i [manualen til `git add`](https://git-scm.com/docs/git-add). 

### Bisect

`git bisect` er et utrolig nyttig verktøy for debugging. Hvis du ønsker å finne hvilken commit som har introdusert en feil, men `git bisect` gjøre et automatisk halveringssøk gjennom historikken din for å finne den commiten som introduserer feilen. 

[Kapittelet om debugging med Git](https://git-scm.com/book/en/v2/Git-Tools-Debugging-with-Git) i Pro Git gir en god intro til `git bisect`.

