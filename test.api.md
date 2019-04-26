// Create new dataset with and without fields

<% assign dataset.id = 'test1000' %>                      // Mandatory
<% assign dataset.name = 'Test 1000' %>                  // Mandatory
<% assign dataset.description = 'Test 1000 dataset' %>    // Optional

// delete the dataset if exists.
<% en.data.sets.delete results dataset.id %>
<% return 'test1000-delete' results %>

// Create the dataset
<% en.data.sets.create results dataset %>
<% return 'test1000-create' results %>

<% assign dataset.id = 'test1001' %>                        // Mandatory
<% assign dataset.name = 'Test 1001' %>                     // Mandatory
<% assign dataset.description = 'Test 1001 dataset' %>      // Optional

<% assign field1.id = 'firstName' %>                        // Mandatory
<% assign field1.name = 'First Name' %>                     // Mandatory
<% assign field1.dataType = 'STRING' %>                     // Optional, default:STRING
<% assign field1.uiType = 'TEXTBOX' %>                      // Optional, default:TEXTBOX

<% assign field2.id = 'phone' %>                            // Mandatory
<% assign field2.name = 'Phone' %>                          // Mandatory
<% assign field2.dataType = 'STRING' %>                     // Optional, default:STRING
<% assign field2.uiType = 'TEXTBOX' %>                      // Optional, default:TEXTBOX

//If fields available, then that will be used. Otherwise 2 default name, description fields will be created.
<% assign dataset.fields = [field1,field2] %>      // Optional

// delete the dataset if exists.
<% en.data.sets.delete results dataset.id %>
<% return 'test1001-delete' results %>

// Create the dataset
<% en.data.sets.create results dataset %>
<% return 'test1001-create' results %>



