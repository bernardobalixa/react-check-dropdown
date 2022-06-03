# React Check Dropdown
Do a dropdown with checkboxes if you want to select multiple options.
## Props
| Name  | Type | Description | Default |
| :-: | :-: | :-: | :-: |
| color | string | Choose the color of the dropdown | "black" |
| title | string | The text that will show in the dropdown | "Check Dropdown" |
| list | array | Need to be an array of objects with the icon(optional), value and label | Required |
| listCheck | object | Need to be an object with the keys equal to **list** values | Required |
| setListCheck | func | The function that will set the **listCheck** state | Required |
## Usability
Here how you can implement it:
```javascript
...
import CheckDropdown from './components/checkdropdown';
...
// Example List
const items=[
  {
    value: "sport", 
    label: "Sport"
  },
  {
    value: "videogames",
    label: "Play video games"
  },
  {
    value: "read", 
    label: "Read"
  }
]

// Example Initial List
const initialList = {
  sport: false,
  videogames: false,
  read: false
}

function ExampleComponent(props){
  const [listCheck, setListCheck] = useState(initialListCheck);

  return (
    <div className="ExampleComponent">
      <CheckDropdown
        title="Hobbies"
        list={items}
        listCheck={listCheck}
        setListCheck={setListCheck}
        />
    </div>
  );
}
...
```
You can also add a color to your CheckDropdown like:
```javascript
...
<CheckDropdown
  color="#6e6e6e"
  ...
  />
...
```
And if you want to add some icons to your items you can putting an element in **icon** field of items list:
```javascript
const items=[
  {
    icon: <i className="fas fa-baseball"></i>,
    value: "sport", 
    label: "Sport"
  },
  {
    icon: <i className="fas fa-gamepad"></i>,
    value: "videogames",
    label: "Play video games"
  },
  {
    icon: <i className="fas fa-book"></i>,
    value: "read", 
    label: "Read"
  }
]
```











