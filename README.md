# Regex : `Ex`pressions `rég`ulières

## Les Caractères Littéraux
Les caractères littéraux correspondent exactement à eux-mêmes. Par exemple, la regex **`/abc/`** correspondra à la chaîne **`"abc"`**.

## Les Classes de Caractères
Vous pouvez définir des classes de caractères en utilisant des crochets. Par exemple, **`[aeiou]`** correspondra à **`n'importe quelle voyelle`**. Vous pouvez également spécifier des plages, comme **`[a-z]`** pour toutes les lettres minuscules.

## Les Quantificateurs 
Vous pouvez spécifier la répétition d'un caractère ou d'une classe de caractères en utilisant des quantificateurs. Par exemple, **`a{3}`** correspondra à la chaîne **`"aaa"`**.

## Les Caractères d'échappement
Certains caractères ont une signification spéciale dans les regex (comme **`.`** ou **`*`**). Pour les inclure littéralement, vous devez les échapper avec un backslash **`\`**.

## Les Ancres 
**`^`** correspond au début d'une chaîne, et **`$`** à la fin. Par exemple, **`^abc$`** correspondra uniquement à la chaîne "abc" dans son intégralité.

## Les Modificateurs
Vous pouvez ajouter des modificateurs à la fin de votre regex pour changer son comportement. Par exemple, **i** pour rendre la correspondance insensible à la casse.

## Voici un exemple simple où nous construisons une regex pour valider un numéro de téléphone simple : `au format xxx-xxxx`

```js
let regex = /^\d{3}-\d{4}$/;
let phoneNumber = "123-4567";

if (regex.test(phoneNumber)) {
    console.log("Le numéro de téléphone est valide !");
} else {
    console.log("Le numéro de téléphone n'est pas valide.");
}
```
Dans cet exemple, **`^\d{3}-\d{4}$`** signifie :

- **`^`** : Début de la chaîne.
- **`\d{3}`** : Trois chiffres.
- **`-`** : Le caractère tiret.
- **`\d{4}`** : Quatre chiffres.
- **`$`** : Fin de la chaîne.
