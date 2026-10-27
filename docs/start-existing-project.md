# Prompt: starting work on an existing project

Paste this into a new Claude session opened in the project folder, after the plugin is installed for it (see the
README). Fill in the `<…>` parts first.

```text
Šis ir esošs projekts: <nosaukums>, mape <ceļš>. <Viens teikums: kas tas ir.> Šajā sesijā gribu: <mērķis>.

Projektam ir pieslēgts mans harness plugin (ervinsapinis/agent-harness). Tas ir pilots: pārbaudām, vai harness strādā bez iepriekšēja konteksta.

0. Vispirms pārbaudi, vai harness ir aktīvs: vai ir output style "deliberate" un skilli /harness:init un /harness:decide. Ja nav, apstājies un pasaki man.

1. Palaid /harness:init šim projektam un ievēro tā soļus:
   - Faktus ņem no koda un pie katra norādi avota failu. Neprasi to, uz ko atbild kods.
   - Ja projektā jau ir CLAUDE.md, AGENTS.md vai .claude, neko nepārraksti, bet izmaiņas piedāvā kā melnrakstu.
   - Konvencijas nolasi no koda ar skaitļiem (piem., „32 no 34"), parādi sarakstu un prasi vienu apstiprinājumu. Par katru nevienotību pajautā vienreiz, kad pirmo reizi tai pieskaries.
   - Katrai zonai nosaki pārbaudes kāpnes R1–R4. Spēlei vai modam lielākoties būs R4: uzraksti man 3–5 soļu pārbaudi, ko izdarīt spēlē.

2. Jautāšana:
   - Skaidro latviski un vienkārši. Vienā jautājumā tikai viens lēmums, ar konkrētu piemēru no šī projekta.
   - Dod līdz 3 īstiem variantiem, ieteicamo pirmo. „Cits" ir mans paša variants. Mākslīgus variantus nepievieno.
   - Katru manu atbildi pieraksti ar /harness:decide, pirms rīkojies.

3. Ierobežojumi:
   - Bez mana „jā" neko neieraksti diskā. Necommito un nepushoji, ja es to nepalūdzu.
   - Projektā nedrīkst nonākt nekas no mana darba: ne darba devējs, ne klienti, ne darba kods.
   - Ja repo ir publisks, neieraksti tajā neko, kas mani identificē vairāk, nekā repo jau rāda.
   - Taupi tokenus: lasi fragmentus un izmanto grep, nelasi lielus failus visus, paskaidro īsi.
   - Review aģentu palaid tikai tad, ja es to palūdzu.

4. Beigās uzraksti:
   - ko izlēmām;
   - kas palika rindā;
   - ko izlēmi pats (1. līmenis);
   - sadaļu „Harness atradumi": kas protokolā, init vai decide nestrādāja vai bija neskaidrs.
   Pašu plugin nelabo. Atradumus es salabošu agent-harness repo.
```
