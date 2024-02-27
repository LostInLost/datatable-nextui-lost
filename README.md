
# Data Table NextUI (Beta)

A Super Data Table Utils like datatable but with integration with NextUI and FontAwesome

## Installation

Make sure you already install NextUI and FontAwesome

```bash
  npm i datatable-nextui-lost
```

## Usage/Examples

```javascript
import DataTable from 'datatable-nextui-lost'
const data = [
    {
      key: 1,
      no: 1,
      name: 'Losinto',
      status: 'Active',
      action: <Button color="warning">Edit</Button>,
    },
  ];
function App() {
  return <DataTable columns={['Name', 'Status', 'Action']} data={data} />
}
```

### Data Format

```javascript
import DataTable from 'datatable-nextui-lost'
...
const data = [
    {
      key: 1, (Required)
      no: 1, (Required)
      ...columns: ...values,
    },
  ];
```

example :

```javascript
import DataTable from 'datatable-nextui-lost'
...
const data = [
    {
      key: 1,
      no: 1,
      name: 'Losinto',
      status: 'Active',
    },
  ];

function App() {
  return <DataTable columns={['Name', 'Status']} data={data} />
}
```

if you want to add a JSX Element in you column like a edit or delete button, you can add like this :


```javascript
import DataTable from 'datatable-nextui-lost'
...
const data = [
    {
      key: 1,
      no: 1,
      name: 'Losinto',
      status: 'Active',
      action: <Button color="warning">Edit</Button>,
    },
  ];
  return (
    <div className="p-10">
      <DataTable columns={['Name', 'Status', 'Action']} data={data} />
    </div>
  );
```
![image](https://github.com/LostInLost/datatable-nextui-lost/assets/103498496/2fab8f11-3f74-471a-8056-1b8b45586f71)

### Searchable

if you want to enable searchable on the DataTable NextUI Lost, you can add "isSearchable" props like this :

```javascript
import DataTable from 'datatable-nextui-lost';
...
<DataTable columns={['Name', 'Status', 'Action']} isSearchable data={data} />
```

But, you must add the "searchFilterColumn" to make the search find your data like this :

```javascript
import DataTable from 'datatable-nextui-lost';
...
<DataTable columns={['Name', 'Status', 'Action']} isSearchable data={data} searchFilterColumn={['Name']} />
```
Don't worry, if you want to make a many column to search, you can add it, its array.
#### Note : make sure your searchFilterColumn is same with a columns values

![image](https://github.com/LostInLost/datatable-nextui-lost/assets/103498496/90f24d6a-6bca-4549-8de7-d78ffd6c0b68)

![image](https://github.com/LostInLost/datatable-nextui-lost/assets/103498496/bc6b0d2f-ad3e-4fc6-85b5-d7e1595c0df8)

### Extra Content

You maybe want to add like button "Add User" to add, so we make the extraContent to you to add your extra content like this :

```javascript
import { Button } from '@nextui-org/react';
import DataTable from 'datatable-nextui-lost';
...
  const AddUser = () => {
    return <Button color='primary'>Add User</Button>
  }

  return (
    <div className="p-10">
      <DataTable 
      columns={['Name', 'Status', 'Action']} 
      isSearchable 
      data={data} 
      searchFilterColumn={['Name']} 
      extraContent={<AddUser />} />
    </div>
  );
```

![image](https://github.com/LostInLost/datatable-nextui-lost/assets/103498496/d9d5c77d-08b2-4101-9b15-836943c298e9)

### End Credit
Support to : NextUI, FontAwesome, and Me:)

Donation for Supports:

https://sociabuzz.com/fanandha35

https://saweria.co/LosintoPalamos

Thanks for using:)


## Authors

- [@LostInLost](https://github.com/LostInLost)




