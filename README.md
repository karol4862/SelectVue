# vselect

## Install
```
npm i @karol4862/vselect
```
## Import 
```
import { vSelectComponent } from '@karol4862/vselect/src';
```
## Usage

```
<template>
  <div>
    <vSelectComponent v-model="results" :options="options" label="value" requiredForm/>
  </div>
</template>
```
```
export default {
  data() {
    return {
      options: [{
        id: 1,
        value: 'option 1',
      },
      ],
    };
  }
}
```

### Props

| Prop | Description |
| --- | --- |
| options | Array with elements to render |
| label | One of the variables will be displayed|
| requiredForm | If true, form will require this section |
| searchable | Set a number, if there are more options than a set number search is available, default is 10 |
| multiple | Multi select |
