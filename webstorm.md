# Webstorm Live Templates

## File Templates


### Reducer

```
export interface #[[$Entity$]]# {
  id: number;
}

export interface #[[$Entity$]]#Items {
  [key: number]: #[[$Entity$]]#;
}

export interface #[[$Entity$]]#State {
  items: #[[$Entity$]]#Items;
}

export type Set#[[$Entity$]]#sAction = Action<'#[[$SET_ACTION$]]#', #[[$Entity$]]#Items>;
export const set#[[$Entity$]]#s = (items: #[[$Entity$]]#Items): Set#[[$Entity$]]#sAction => ({type: '#[[$SET_ACTION$]]#', data: items});

export type #[[$Entity$]]#Actions = Set#[[$Entity$]]#sAction;

function #[[$LowerEntity$]]#Items(state: #[[$Entity$]]#Items = {}, action: #[[$Entity$]]#Actions) {
  switch (action.type) {
    case '#[[$SET_ACTION$]]#': return action.data;
    default: return state;
  }
}

export const #[[$LowerEntity$]]#s = combineReducers<#[[$Entity$]]#State>({
  items: #[[$LowerEntity$]]#Items
});

export const get#[[$Entity$]]#Items = (state: CommonState) => state.entities.#[[$LowerEntity$]]#s.items;
export const get#[[$Entity$]]#sArray = (state: CommonState): #[[$Entity$]]#[] => Object.values(get#[[$Entity$]]#Items(state));
```
