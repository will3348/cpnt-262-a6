# cpnt-262-a6
### Will Tengyuan Li
### Plan
- Create vue component (header,footer), add to app.vue
- Use moustache syntax to render information that is stored in the script tag of the component
- add slot
- list component
-  Create a computed property 
### Todo
- I created a vue project. Then added TheHeader.vue and TheFooter.vue to component folder. 
```javascript
export default {
  data() {
    return {
      message: 'Hello World!'
    }
  }
}
```
- import to app.vue
```javascript
import ComponentA from './ComponentA.vue'
```
- added a slot in <TheHeader></TheHeader>, fill in a h2


![](./src/assets/headerslot.png)

![](./src/assets/headerslot1.png)
- Then I created a list component in app.vue
```javascript
<ol class="myList">
      <li v-for="item in sortList" v-bind:key="item.title">
        {{ item.title }}
      </li>
    </ol>
``` 
- Then script
![](./src/assets/listcomponent.png.png)
- my friend Spark helped me to create a computed property that renders a modified version of the list
![](./src/assets/computed.png)