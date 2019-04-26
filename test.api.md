# Create new dataset with default fields

## Define dataset object
```
<% assign dataset.id = 'test1000' %>                     // Mandatory
<% assign dataset.name = 'Test 1000' %>                  // Mandatory
<% assign dataset.description = 'Test 1000 dataset' %>   // Optional
```

## delete the dataset if exists.
```
<% en.data.sets.delete results dataset.id %>
<% return 'test1000-delete' results %>
```

## Create new dataset with default fields
```
<% en.data.sets.create results dataset %>
```
## return the results
```
<% return 'test1000-create' results %>
```
