AINXPGS — WEB DE PROMOCIÓ DE VINTED

CONTINGUT
- index.html: pàgina principal
- styles.css: disseny responsive
- app.js: traduccions ES / CA / EN / FR i targetes de producte
- products.js: articles que vols destacar
- README.txt: aquestes instruccions

A. PROVAR LA WEB AL TEU ORDINADOR
1. Descomprimeix el fitxer ZIP.
2. Obre index.html amb Chrome, Edge o Firefox.
3. Canvia l'idioma amb el selector ES / CA / EN / FR.
4. Els botons principals obren el teu perfil:
   https://www.vinted.es/member/3166248614-ainxpgs

B. PUBLICAR-LA GRATIS A CLOUDFLARE PAGES
1. Ves a https://dash.cloudflare.com/ i crea un compte gratuït o inicia sessió.
2. Obre Workers & Pages (o Pages) i tria Create application / Create project.
3. Tria l'opció de pujar assets estàtics (Direct Upload / Upload assets; el nom pot variar).
4. Puja els fitxers de la web descomprimits. Assegura't que index.html, styles.css, app.js i products.js quedin a l'arrel de la publicació, no dins d'una subcarpeta addicional.
5. Posa un nom al projecte, per exemple ainxpgs-vinted.
6. Prem Deploy. Cloudflare t'assignarà una adreça acabada en .pages.dev.
7. Obre l'adreça en mòbil i ordinador i comprova els quatre idiomes i els enllaços a Vinted.

Nota: Cloudflare pot canviar lleugerament els noms dels botons de la interfície. Documentació oficial:
https://developers.cloudflare.com/pages/framework-guides/deploy-anything/

C. AFEGIR ARTICLES DESTACATS
Edita products.js i afegeix-hi els articles que vulguis mostrar. Exemple:

window.VINTED_PRODUCTS = [
  {
    name: "Jaqueta texana",
    description: "Bon estat · Talla M",
    price: "18 €",
    image: "images/jaqueta.jpg",
    url: "https://www.vinted.es/items/ID-ARTICLE"
  }
];

- Crea una carpeta images i desa-hi les fotos que tinguis dret a publicar.
- Substitueix ID-ARTICLE per l'enllaç real de l'anunci.
- Desa products.js i torna a publicar els fitxers actualitzats a Cloudflare Pages.
- Si encara no tens articles afegits, la web mostra un missatge d'exemple a la secció de selecció.

D. IMPORTACIÓ AUTOMÀTICA DES DE VINTED
La documentació oficial de Vinted Pro Integrations indica que:
- L'API està restringida a comptes professionals autoritzats (allowlisted).
- L'API permet gestionar articles i sincronitzar inventari.
- Per importar anuncis que ja existeixen al compte Vinted i que no es van publicar via aquesta integració, Vinted indica que cal contactar amb el gestor de compte.

Documentació:
https://pro-docs.svc.vinted.com/
Portal:
https://pro-portal.svc.vinted.com/

Passos recomanats:
1. Comprova si el teu compte pot ser Vinted Pro i si tens gestor de compte.
2. Contacta amb Vinted Pro i pregunta específicament si et poden autoritzar Vinted Pro Integrations i importar/sincronitzar els anuncis existents del compte ainxpgs.
3. No comparteixis contrasenya, cookies de sessió ni codis d'accés amb serveis de tercers.
4. No farem scraping ni bots no autoritzats.
5. Si Vinted confirma l'accés, caldrà implementar una integració segura al servidor. No s'han de posar tokens/API secrets dins dels fitxers públics HTML o JavaScript.

LIMITACIÓ ACTUAL
Aquesta és una web promocional independent; els anuncis no se sincronitzen automàticament en aquesta versió. Els enllaços de producte porten a l'anunci real de Vinted quan afegeixes la seva URL a products.js.

PERSONALITZACIÓ DE CONFIANÇA:
La pàgina inclou una secció fixa que explica que les compres es fan a Vinted, que el perfil mostra verificacions i que els preus són negociables. Les dades no s'actualitzen automàticament.
La secció "Els meus preferits" està preparada per mostrar articles seleccionats manualment. Per afegir els favorits definitius, cal posar els seus títols, fotos, preus i enllaços a products.js.

SELECCIÓ FIXA INICIAL:
products.js ara inclou 20 articles seleccionats visualment de les captures aportades, amb miniatures extretes d'aquestes captures. Els enllaços van al perfil general perquè les captures no proporcionen les URL individuals. Revisa els noms i completa preus/enllaços exactes abans de publicar.

SELECCIÓ DEFINITIVA DEMANADA:
products.js mostra només els 9 articles de les captures més recents: pantalons rosa i blau, dues jaquetes, sabatilles, dos pantalons/texans, estotjos Cedon i Apple iMac. Els preus són els visibles a les captures. Els botons enllacen al perfil general perquè no disposem dels URL individuals.
