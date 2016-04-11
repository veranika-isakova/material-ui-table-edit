# material-ui-table-edit
Material UI Table Edit

<img src="https://raw.githubusercontent.com/emkay/material-ui-table-edit/master/example/table-editor.gif">

## Install

`npm i material-ui-table-edit`

## Usage

```javascript
const React = require('react')
const ReactDOM = require('react-dom')
const EditTable = require('../index.jsx')
const container = document.createElement('div')

document.body.appendChild(container)
const headers = [
  {value: 'Name', type: 'TextField', width: 200},
  {value: 'Address', type: 'TextField', width: 200},
  {value: 'Phone', type: 'TextField', width: 200},
  {value: 'Enabled', type: 'Toggle', width: 50},
  {value: 'Last Edited By', type: 'ReadOnly', width: 100}
]

const rows = [
  {columns: [
    {value: 'Michael'},
    {value: '1212 Somewhere st.'},
    {value: '555-1212'},
    {value: false},
    {value: 'Michael at 4:20pm'}
  ]},
  {columns: [
    {value: 'Sara'},
    {value: '1212 Somewhere st.'},
    {value: '555-1212'},
    {value: true},
    {value: 'Someone at 5:50pm'}
  ]},
  {columns: [
    {value: 'Randy Randerson'},
    {value: '5555 Somewhere st.'},
    {value: '888-555-3333'},
    {value: true},
    {value: 'Randy at 3:33pm'}
  ]}
]

const onChange = (row) => {
  console.log(row)
}

ReactDOM.render(
  <EditTable
    onChange={onChange}
    rows={rows}
    headerColumns={headers}
  />,
  container
)
```
