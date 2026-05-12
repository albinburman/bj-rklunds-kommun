\# Logbook — Björklunda kommun Del 1

\*\*Namn:\*\* Albin Burman

\*\*E-post:\*\* albbur051026@student.jenseneducation.se

\*\*Inlämning:\*\* Del 1 



\# Arbetslogg --# 2026-04-24

\*\*Arbetat med: uppgift #1\*\*

\*\*Vad jag gjorde:Jag skapade ett konto på redhat samt laddade ner ISO filen via deras webbsida. Sen så installerade jag git på min dator och la in mitt namn samt epost och startade gita i mappen Burman\_Albin\_privat1 för att kunna ha koll och logga det jag gör i dom olika under mapparna i framtiden. Sen så skapade jag signatur skriptet både för powershell och Linux. Först gjorde jag en initial commit där jag la upp repo strukturen och template för loggboken jag skriver i nu. Sen så gjorde jag en commit där jag la till dom 2 olika scripten.

\*\*

\*\*Problem och lösningar: hitta rätt version av redhat.\*\*

\*\*Beslut jag fattade: inga riktiga beslut\*\*

\*\*Källor jag använde: copilot ai \*\*



\# Arbetslogg --# 2026-05-08

\*\*Arbetat med: uppgift #1\*\*

\*\* Vad jag gjorde: bestämde partition och läste på massor om redhat. 

\*\*Problem och lösningar: Jag hade svårt att bestämma mig om hur jag skulle partionera

men med hjälp av en klasskamrat förstod jag vad jag ska lägga vikt på osv.\*\*

\*\*Beslut jag fattade: partionering\*\*

\*\*Källor jag använde: copilot ai, Anton haha \*\*



\# Arbetslogg --# 2026-05-11

\*\*Arbetat med: uppgift 1 del 2 och 3\*\*

\*\* Vad jag gjorde: konfigurerade redhat skicka över mitt bash script från powershell genom ssh.

\*\*Problem och lösningar: Svårt att få till överföringen av bash scriptet från Powershell till srv-linux01 då jag hade problem med brandväggen och att jag gjort en txt fil på powershell

men med hjälp av ai och sunt förnuft förstod jag hur jag skulle åtgärda detta.\*\*

\*\*Beslut jag fattade:\*\*

\*\*Källor jag använde: copilot ai, redhat forum \*\*





\# Del 1

\# Del 2 — Planering -

Red hat rekomenderar att använda minst 1GB utrymme för att kunna rymma fler kernelversioner

XFS är standard i RHEL 7/8/9 och gjort för stora filstystem flera hundra TB medans ext4 är mer traditionellt allround och stödjer filer upp till 16TB och system upp till 50TB enligt den här artikeln https://access.redhat.com/articles/3129891 RHEL idM är redhats användar hanterare och är typ som linux active directory. Jag blev förvirrad av alla nya begrepp och förstod inte helt vart jag skulle börja osv.



Srv-idm01

Eftersom IdM‑servern hanterar LDAP‑databas, Kerberos, certifikat och loggar kräver den mer utrymme i /var än en vanlig server. Därför valde jag att öka root‑partitionen från 20 GB till 30 GB för att ge tillräckligt med utrymme för användar hanteringen.

alltså kommer jag partitionera såhär. 

/Boot 1GB

/ 30GB

/home 10Gb

swap 2GB



srv-linux01 

jag har valt att köra allt på minimum här för att inte sno för mycket utrymme från min dator och för att jag inte tror att det behövs men vi får se i framtiden.

/Boot 1GB

/ 20GB

/home 10GB

swap 2GB





\# Del 3 — Linux-serverinstallation 

jag väljer att köra mina virtuella maskiner på ett bridged nätverk så att alla kan kommunicera med varandra enkelt. 



skärmdump-3 (screenshots)

skärmdump-4 (screenshots)

skärmdump-5 (screenshots)

skärmdump-6 (screenshots)



frågor och svar del 3.4.3

1. networkmanager.service är Linux nätverkshanterare och sköter saker som dhcp och vpn.
2. standard inställningen för ssh är port 22.
3. om man stängde av en kritisk tjänst som tex networkmanager så skulle ingen som var kopplad till servern få en ip adress och då alltså inte kunna använda internet.



skärmdump-7 (screenshots)







\# Del 4 — Windows Server och Active Directory -

\# Del 5 — Kontohantering med script -

\# Del 6 — Delade mappar och rättigheter -

\# Del 7 — Utskriftssystem -

\# Del 8 — Virtualisering -

\# Del 9 — Lagar och säkerhet -

\# Del 10 — Råd och stöd -

\# Del 11 — Reflektera över din miljö

