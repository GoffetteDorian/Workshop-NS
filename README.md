# Workshop Nativescript

Bonjour à tous,

Pour ce workshop vous aurez besoin d'un Smartphone (Apple ou Android, au choix) branché a votre pc et installer les applications suivantes:

- Nativescript Playground qui vous permettra de scanner le QR code pour linker votre application en développement a votre Smartphone
- Nativescript Preview qui vous permettra d'afficher le rendu de l'application développée

Vous pouvez voir le rendu de votre application de 2 manières:

- En effectuant un tns preview, vous scannez le QR code avec l'application Preview et votre code sera affiché sur votre smartphone
- En effectuant un tns run (android ou ios) --bundle, le CLI scannera tout les devices connectés a votre machine et simulera l'application dessus. Ceci nécéssite un smartphone en mode developpeur (Cliquer plusieurs fois sur la version de votre smartphone dans les paramètres) branché a votre pc ainsi que le Débuggage USB (options développeurs) activé.

L'**installation** de tout l'environnement travail :

- Premièrement, il vous faudra Nativescript.

```bash
  npm install -g nativescript
```

- Verifiez l'installation

```bash
  tns doctor
  tns create testapp
  cd testapp
  tns run android #ios depending on your smartphone
```

- Ensuite, vous aurez besoin de Vue CLI

```bash
  npm install -g @vue/cli @vue/cli-init
  vue init nativescript-vue/vue-cli-template loginApp
```

- Lancez la compilation

```bash
  cd loginApp
  npm install
  tns run android --bundle #ios depending on your smartphone
```

Un autre point assez important, Nativescript peut s'utiliser avec plusieurs _Frameworks_ ou _Supersets_, les plus populaires étant React et Typescript. Pour ce workshop nous utiliserons **VueJS**.

[Documentation Nativescript VueJS](https://nativescript-vue.org/en/docs/introduction/)

Il est possible de se passer de son Smartphone en utilisant des emulateurs, ceux-ci étant long à installer. Je ne m'attarderai pas sur l'installation et la configuration de ceux-ci dans mon workshop, mais dans le cas ou vous voudriez continuer à travailler avec un émulateur par la suite, n'hésitez pas a me demander.
