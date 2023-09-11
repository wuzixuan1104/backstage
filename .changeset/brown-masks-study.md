---
'@backstage/plugin-catalog-backend': minor
---

Deprecated the old `BuiltinKindsEntityProcessor` class. Please import it as
`SystemEntityModelProcessor` from
`@backstage/plugin-catalog-backend-module-system-entity-model` instead, if you
use it explicitly.

**BREAKING** (in the alpha exports for the new backend system): _For the new
backend system specifically_, you now have to add the
`catalogModuleSystemEntityModel` to your backend along with the catalog backend
plugin itself, if you want to keep using the default model.

```diff
 import { catalogPlugin } from '@backstage/plugin-catalog-backend/alpha';
+import { catalogModuleSystemEntityModel } from '@backstage/plugin-catalog-backend-module-system-entity-model/alpha';

 const backend = createBackend();
 backend.add(catalogPlugin());
+backend.add(catalogModuleSystemEntityModel());
```
