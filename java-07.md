# RideShare — Java 7

## Çfarë ndërtova
Përshkruaj ndryshimin e kësaj jave me fjalët e tua.
Kete jav nuk shtova vecori te reja vetem rregullova nje gabim titulli i skedes tregonte "Create Next App" ndersa tani tregon "RideShare AAB".

## Provat që bëra
### Prova 1: Rrjedha kryesore mund të demonstrohet nga fillimi në fund.
[PLOTËSO] Hapat, rezultati i pritur dhe çfarë ndodhi.
Prita qe tri udhetimet te hyje me GitHub te hape udhetimin 2 dhe te shoh "Simulim Ne pritje" pas "Kerko vend" realisht ndodhi saktesisht keshtu si ne localhost ashtu edhe ne Vercel ndersa udhetimi i 3 jet "Nuk ka vende te lira" me butonin te çaktivizuar.

### Prova 2: Raporti përshkruan një gabim dhe korrigjimin e tij.
Hapat, rezultati i pritur dhe çfarë ndodhi.
Vura re se titulli i skedes ishte "Create Next App" ndryshova ne "RideShare AAB App" pastaj nje tjeter gabim qe u korrigjua hyrja ne Vercel deshtonte sepse mungonin variablat GITHUB_ID, GITHUB_SECRET, NEXTAUTH_SECRET dhe NEXTAUTH_URL; i shtova ne Vercel shtova adresen e callback-ut ne GitHub OAuth App dhe bera Redeploy.


### Prova 3: Mund të shpjegoj ku ruhen të dhënat dhe kush lejohet t’i ndryshojë.
Hapat, rezultati i pritur dhe çfarë ndodhi.
Të dhenat (udhëtimet dhe profilet) ruhen ne databazen Neon (PostgreSQL) serveri i lexon me DATABASE_URL qe mbetet private dhe nuk shkon te shfletuesi oren e udhetimit e ndryshon vetem shoferi qe e zoteron serveri kontrollon sesionin dhe pronarin ne databaze (lib/lejet.ts) jo formularin kur ndryshova ID ne 1 nga DevTools, ruajtja u refuzua.

## Ku gjendet puna
Shëno skedarët kryesorë dhe linkun e demonstrimit nëse është publikuar.
Repository: https://github.com/edonishasani171-eng/rideshare-mobile

## Çfarë mbetet për përmirësim
Një kufizim ose gabim që vure re dhe hapi i ardhshëm.
Kerkesa "Ne pritje" mbetet simulim nuk ruhet kerkese dhe shoferi nuk njoftohet hapi im i ardhshem eshte te shtoj nje tabele kerkesash ne Neon qe udhetari te dergoje kerkese te vertete dhe shoferi ta pranoje ose refuzoje.

## Ndihma nga AI (Artificial Intelligence – inteligjencë artificiale)
Çfarë ndihme more dhe çfarë verifikove vetë, ose: Nuk përdora AI.
Perdora AI per ndihme me ngjitjen e kodit gabimet e build-it dhe konfigurimin e hyrjes ne Vercel provova vete te gjitha hapat ne shfletues ndryshova variablat ne Vercel dhe GitHub dhe kontrollova rezultatet.