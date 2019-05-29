# Datamodel


Het data model ziet er als volgt uit:

Tabel: *profile*
| veldnaam 	|  type 	|
|:--------:	|:-----:	|
| username 	| email 	|
| password  | SALT+SHA256 |
| first_name | varchar:text |
| middle_name |varchar:text |
| last_name | varchar:text |
| phone | number:10 |
| pitch |text |
| insight | array:score |
| big5 | array:score |
| 360 | array:score |
| education | array:tag |
| training | array:tag |
| certificate | array:tag |
| diploma | array:tag |
| skills | array:tag |
| soft_skills | array:tag |
| skill_rating | number:1-100 |
| interests | array:tag |
| work-fields | array:tag |
| motivation | array:tag |
| personality | array:tag |
| available_on | varchar:date |


## Webforms
Dit zijn de webviews met de verwachte velden



### Home

* Logo met link naar home
* Zoek matches [Button]
* Contact [Button]

#### Authenticatie
* Gebruikersnaam [textinput: email]
* Wachtwoord [textinput type:password]
* Registratie [link]


<hr />

### Profiel pagina

#### Management samenvatting
[textarea] Ik ben.... en ik kan ..... [/textarea]

##### Talent Tree
* [image:tree button]
* Storyboard [Button]


##### Wie ben ik?
* Insight (graph)
* Big five (graph)
* 360 (stats)
  * Netjes
  * Gedreven
  * Gemotiveerd
  * Energiezuinig
  
##### Wat kan ik?
* Hard Skills
  * Opleidingen
  * Cursussen
  * Certificaten
  * Diploma's
* Soft Skills
  * Leiderschap
  * Doorzettingsvermogen
 
##### Wat kan wil ik?

* Skill_[competentie_[name]}_Rating --> [0-100% processbar]

* Interesssegebieden
  * management [tag]
  * product owner [tag]

* Werkvelden
  * defensie [tag]
  * landbouw [tag]

* Drijfveren
  * geld [tag]
  * macht [tag]

* Drijfveren
  * geld [tag]
  * macht [tag]

* Functies/posities
  * schoonmaker [tag]
  * directeur [tag]

[button] Vergelijk/Bekijk [button]    [button] Matches >> [button] 

<hr />

### Overzicht vacatures
Pagina met het overzicht met vacatures met de volgende filter mogelijkheden.

#### Profiel
* Skill_[NR}_Rating --> 1 - 10

#### Voorkeuren
* Standplaats
* Salarisschaal
* Duur opdracht
* Beschikbaar per
* Opleidingsniveau

#### Vacature selectie
- [ ] persoonlijkheden
- [X] vaardigheden
- [ ] beschikbaar per

#### Suggesties
- [ ] Vacature A
- [ ] Vacature B
- [ ] Vacature C

#### Toon alles
- [ ] Vacature D
- [ ] Vacature E
- [ ] Vacature F

<hr />

### Vacature
Detail pagina van de vacature.

#### Functie titel 
* Functie [tag]
* Organisatie [tag]
* Locatie [locatie]
* Salaris [euro]
* Arbeidsduur [tijdsblok]
* Start [date]

#### Functie Omschrijving
* [textarea] Omschrijving [/textarea]

#### Match [match_score(%)] 
* Big five (graph)
* Vaardigheiden [tags] -->  (graph)

##### Aanvullende eisen
* Opleiding
* Ervaring

#### Sollicatie 
* Match [match_score(%)] 
* Wil je solliciteren?
* Ja  [Button] --> action: solliciteren  (no geen design)
* Nee [Button] --> actie: terug naar [Overzicht Vactures](https://pages.rijksgithub.nl/SSC-ICT-Innovatie/RCD-Hackathon/Datamodel#overzicht-vacatures)
