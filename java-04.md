# RideShare — Java 4 · Neon dhe PostgreSQL

Ruaje këtë skedar si java-04.md pranë README, jashtë aplikacioni/.
Plotëso të gjitha përgjigjet; hiqi shenjat [PLOTËSO].
Mos vendos DATABASE_URL, pamje të kredencialeve ose të dhëna reale.

## Çfarë ndërtova
Shpjego si lista dhe detajet i lexojnë udhëtimet nga Neon.
Ndertova qe te shfaqet ne list e vendint se nga behet, nisja ne oren e caktuar, takimi i caktuar dhe sa vende jane te lira. 

## Provat që bëra
### Prova 1: Ndryshimi në databazë shfaqet në aplikacion
Shkruaj çfarë tregoi lista dhe çfarë treguan detajet pas rifreskimit.
Ktheje orën në 08:15 dhe provo përsëri.
Ndryshova oren e Id 2 ne editor te Neon nga 08:15 ne 08:25 dhe ne ekran duhej te bej nje rifreskim dhe ndyshimi u be me sukses pastaj e riktheva perseri ne 08:15.

### Prova 2: Lista bosh dhe rikthimi
[PLOTËSO] Shtova WHERE false vetëm te pyetja e lexoUdhetimet.
Shkruaj mesazhin që u shfaq. Hoqe WHERE false dhe u kthyen tri kartat?

### Prova 3: Lidhja mungon, rikthimi dhe siguria
Ndryshova përkohësisht emrin DATABASE_URL në .env.local,
rinisa serverin dhe shënova mesazhin. Riktheva emrin dhe rinisa serverin.
Shkruaj a punoi sërish; a mungon .env.local në listën e GitHub Desktop?
Ndryshova perkohesisht emrin DATABASE_URL ne .env.local, rinisa serverin lidhja u be me sukses. .env.local nuk shfaqet ne listen e ndryshimeve te git prandaj nuk shkon ne github.


## Ku gjendet puna
Shëno schema.sql, skedarët që ndryshove dhe linkun e repository-t.
Nëse punon në Vercel, shto linkun e aplikacionit (opsional këtë javë).
Skedari schema.sql eshte brenda aplikacioni/ prane README.md Skedaret qe ndryshova jane lib/db.ts, lib/udhetimet.ts, app/page.tsx, app/udhetimi/[id]/page.tsx dhe app/udhetimi/[id]/kerkesa/page.tsx. Repository: https://github.com/edonishasani171-eng/rideshare-mobile


## Çfarë mbetet për përmirësim
Një kufizim ose gabim dhe hapi yt i ardhshëm.
Kërkesa “Në pritje” mbetet simulim; nuk ka rezervim real.
Kerkesa "Ne pritje" mbetet simulim nuk ka rezervim real hyrje per shofer ose udhetar hapi im i ardhshem eshte te shtoj nje meny qe shoferi te krijoje udhetime dhe udhetari te dergoje kerkese te vertete.


## Ndihma nga AI (Artificial Intelligence – inteligjencë artificiale)
Çfarë ndihme more dhe çfarë verifikove vetë, ose: Nuk përdora AI.
Perdora AI per te ndihmuar me ngjitjen e kodit dhe gabimin e build-it ne Vercel (shtova export const instant = false) i provova vete te gjitha faqet ne shfletues ekzekutova sql ne Neon dhe kontrollova qe .env.local nuk shkon ne github.