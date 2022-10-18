# QR_menu
 A Menu Base for QRCore
This script allows you create menu like RDR2.

## 1. Installation
- Be sure you have RedEM and RedEM:RP Installed
if not -> [RedEM](https://github.com/kanersps/redem)
- add ```ensure qr_menu``` after ```ensure qr-core```

![alt text](https://i.imgur.com/XwI6mJH.jpeg)

## 2.Usage
Add this on top your client side file
```
MenuData = {}
TriggerEvent("qr_menu:getData",function(call)
    MenuData = call
end)
```
Example:
```
         MenuData.CloseAll()
        local elements = {
 
                {label = "Test Option", value = 'test' , desc = "Press if you want print text"},
        }
 
       MenuData.Open(
 
                'default', GetCurrentResourceName(), 'test_menu',
 
                {
 
                        title    = 'TestMenu',
                        
                        subtext    = 'There is a subtext',
 
                        align    = 'top-left',
 
                        elements = elements,
 
                },
                function(data, menu)

                        if(data.current.value == 'test') then
                               print("test")
                        end
                end,
                
                function(data, menu)
                        menu.close()
              end)  

```

## 3.Credits
- https://github.com/ktos93
- https://github.com/ESX-Org
