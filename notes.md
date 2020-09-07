# app/app.js

Permet d'avoir les logs de vue dans la console.

```
  vue.config.silent = false;
```

Crée une vue qui permettra d'afficher le rendu de LoginPage

```
new Vue({
    render: h => h('frame', [h(LoginPage)])
}).$start();
```

# app/components/LoginPage.vue

```
  <FlexboxLayout />
```

Layout qui permet d'arranger les enfants horizontalement et verticalement.

```
  <StackLayout />
```

Layout qui permet d'empiler des enfants verticalement (par défaut) ou horizontalement

```
  <TextField />
```

v-model -> Associe une variable au champ qui s'actualisera lorsque la variable change
returnKeyType:
-> next pour passer au champ suivant lors du carriage return
-> done pour submit le formulaire
@returnPress -> Event trigger quand le bouton return est appuyé

```
  const userService = {}
```

Coté back-end

```
  const HomePage = {}
```

Normalement ça serait un fichier qui nous dirigerais vers la suite, mais vu qu'on fait que le login, on cree un template rapidement via une variable

## Data

```
  isLoggingIn: true
```

Permet d'afficher les champs nécéssaires entre login et register
true = login && false = register

## Methodes

```
  toggleForm()
```

Change entre login et register

```
  submit()
```

Submit du form, verifie que les champs soient bien remplis, effectue l'action de login ou register en fonction du formulaire rempli

```
  login() et register()
```

Accede au back-end pour effectuer le login et le register et se déplacer vers la homepage

```
  forgotPassword()
```

Affiche une modal qui nous demande l'email de recupération -> reset le password associé a l'email

```
  focusPassword()
  focusConfirmPassword()
```

Set le focus sur le password ou sur la confirmation du password

```
  alert()
```

Modal custom pour les messages d'alertes

## Firebase
