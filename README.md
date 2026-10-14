# imgiainfo.com

Site public de **IMGIAINFO inc.** — plateformes sur mesure : image, IA, information.

Publié par GitHub Pages depuis la branche `gh-pages` (le workflow
`.github/workflows/jekyll-gh-pages.yml` construit le site et le déploie :
**un push sur `gh-pages` suffit**, la page est en ligne une minute plus tard).

## Structure

    _config.yml              titre, description, courriel, téléphone, ville (une seule source)
    _layouts/default.html    la coquille : entete + contenu + pied
    _includes/head.html      metadonnees, favicon, feuille de style
    _includes/nav.html       la navigation (et la bande tricolore)
    _includes/footer.html    le pied de page
    index.html               Accueil
    offre.html               Ce que nous faisons
    alcoa.html               C'est quoi ALCOA++
    ia-de-confiance.html     Un LLM dans la boucle, sans briser ALCOA++
    questions.html           Questions frequentes
    contact.html             Nous joindre
    404.html                 Page introuvable
    assets/css/style.css     toute la mise en page (aucune dependance externe)

## Regles du site

- **Francais**, conformement a la Charte de la langue francaise. Les documents clients peuvent
  etre livres en anglais.
- **Le sigle s'ecrit ALCOA++**, avec deux signes plus, partout.
- **Aucun element externe** : aucune police distante, aucun script, aucun traceur, aucune
  bibliotheque. Le site ne charge que ses propres fichiers.
- **IMG + IA + INFO** sort en trois couleurs (vert, rouge, bleu) : c'est la marque, elle doit
  rester lisible en typographie.

## Modifier le site

    git clone https://github.com/imgiainfo/imgiainfo.github.io
    cd imgiainfo.github.io && git checkout gh-pages
    # modifier les .html ou _config.yml
    git add -A && git commit -m "..." && git push origin gh-pages

Les pages sont ecrites en HTML avec l'entete Jekyll (`--- layout: default ---`). Le contenu se
modifie directement dans le fichier de la page ; les coordonnees se modifient dans `_config.yml`
seulement.
