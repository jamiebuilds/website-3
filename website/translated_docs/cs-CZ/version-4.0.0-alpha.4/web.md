---
id: version-4.0.0-alpha.4-webui
title: Webové uživatelské rozhraní
original_id: webui
---
![Uplinks](https://user-images.githubusercontent.com/558752/52916111-fa4ba980-32db-11e9-8a64-f4e06eb920b3.png)

Verdaccio má webové uživatelské rozhraní pro zobrazení pouze soukromých balíčků a lze je přizpůsobit.

```yaml
web:
  enable: true
  title: Verdaccio
  logo: logo.png
  gravatar: true | false
  scope: @scope
  sort_packages: asc | desc
```

Všechna omezení přístupu definovaná v [ochraně balíčků](protect-your-dependencies.md) se budou vztahovat také na webové rozhraní.

### Konfigurace

| Vlastnost     | Typ        | Požadované | Příklad                        | Podpora  | Popis                                                                                                                                                |
| ------------- | ---------- | ---------- | ------------------------------ | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| enable        | boolean    | Ne         | true/false                     | všechny  | povolit zobrazení webového rozhraní                                                                                                                  |
| title         | řetězec    | Ne         | Verdaccio                      | všechny  | Popis názvu hlavičky HTML                                                                                                                            |
| gravatar      | boolean    | Ne         | true                           | `>v4` | Gravatary budou vygenerovány pod kapotou, pokud je tato vlastnost povolena                                                                           |
| sort_packages | [asc,desc] | Ne         | asc                            | `>v4` | Gravatary budou vygenerovány pod kapotou, pokud je tato vlastnost povolena                                                                           |
| logo          | řetězec    | Ne         | http://my.logo.domain/logo.png | všechny  | uRI, kde se nachází logo (logo hlavičky)                                                                                                             |
| scope         | řetězec    | Ne         | \\@myscope                   | všechny  | If you're using this registry for a specific module scope, specify that scope to set it in the webui instructions header (note: escape @ with \\@) |

> Doporučuje se, aby velikost loga měla velikost `40x40` pixelů.