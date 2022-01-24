# Development conventions

# VUEX
```js
**!ACTIONS!**
export const ACTION_NAME = 'namespace/actionName';

export const actions = {
  [ACTION_NAME]: (context, ...) => {
    **...code...**
  },
};

**!MUTATIONS!**
export const MUTATION_NAME = 'MUTATION_NAME';

export const mutations = {
  [MUTATION_NAME]: (state, ...) => {
    **...code...**
  },
};

**!GETTERS!**
export const GETTER_NAME = 'namespace/getterName';

export const getters = {
  [GETTER_NAME]: (state) => state.(stateName),
};

**!STORE!**
import { getters } from './getters';
import { mutations } from './mutations';
import { actions } from './actions';

export const getInitialState = () => ({
  **...initial state...**
});

const state = {
  ...getInitialState(),
};

export default {
  state,
  getters,
  mutations,
  actions,
};

## VUEX structer
-store
--store_sub_directory
---actions.js
---mutations.js
---getters.js
---store.js
--index.js


# NAMING
Functions && Methods - CamelCase
Enum - uppercase


