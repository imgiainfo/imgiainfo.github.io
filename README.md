# imgiainfo.com

Site public de **IMGIAINFO inc.** — plateformes sur mesure : image, IA, information.

Bilingue **français / anglais** : le français à la racine, l'anglais sous `/en/`. Chaque page
porte son alternance (`alt`, `alt_fr`, `alt_en`), le sélecteur de langue dans la navigation et
les balises `hreflang` dans l'entête.

Publié par GitHub Pages depuis la branche `gh-pages` (le workflow
`.github/workflows/jekyll-gh-pages.yml` construit le site et le déploie :
**un push sur `gh-pages` suffit**, la page est en ligne une minute plus tard).

## Structure

    _config.yml              titre, description, courriel, ville (une seule source)
    _layouts/default.html    la coquille : entete + contenu + pied
    _includes/head.html      metadonnees, hreflang, favicon, feuille de style
    _includes/nav.html       la navigation bilingue + le selecteur de langue + la bande tricolore
    _includes/marque.html    la marque « iii » (trois tiges, trois points colores)
    _includes/footer.html    le pied de page, bilingue
    index.html               Accueil                       /en/               Home
    offre.html               Ce que nous faisons           /en/what-we-do/
    alcoa.html               C'est quoi ALCOA++            /en/alcoa/
    ia-de-confiance.html     Un LLM dans la boucle         /en/trusted-ai/
    souverainete.html        Souverainete numerique        /en/sovereignty/
    questions.html           Questions frequentes          /en/questions/
    contact.html             Nous joindre                  /en/contact/
    404.html                 Page introuvable
    assets/css/style.css     toute la mise en page (aucune dependance externe)

## Regles du site

- **Francais par defaut, anglais sous `/en/`** : conformement a la Charte de la langue francaise,
  le francais reste la langue principale du site ; l'anglais est une version, pas un remplacement.
- **Le sigle s'ecrit ALCOA++**, avec deux signes plus, partout.
- **Aucun element externe** : aucune police distante, aucun script, aucun traceur, aucune
  bibliotheque, aucun CDN. Le site ne charge que ses propres fichiers — c'est aussi ce que la page
  Souverainete affirme, et la console du navigateur le verifie.
- **Aucun nom de personne, aucun telephone** : le site parle au nom de la compagnie. Le courriel
  `info@imgiainfo.com` est le seul canal indique.
- **IMG + IA + INFO sort en trois couleurs** (vert, rouge, bleu), et la marque « iii » (les trois
  tiges a points colores, comme sur la carte d'affaires) ouvre l'entete et le pied de page.

## Modifier le site

    git clone https://github.com/imgiainfo/imgiainfo.github.io
    cd imgiainfo.github.io && git checkout gh-pages
    # modifier les .html ou _config.yml
    git add -A && git commit -m "..." && git push origin gh-pages

Chaque page est ecrite en HTML avec son entete Jekyll : `--- layout: default ---` plus `lang`,
`title`, `description`, `permalink`, `alt`, `alt_fr`, `alt_en`. Pour ajouter une page, il faut
les **deux** versions et leurs renvois croises. Les coordonnees se modifient dans `_config.yml`
seulement.
