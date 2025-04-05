   ____            _          _        _____                       
  / __ \          (_)        | |      |  __ \                      
 | |  | |  _   _   _    ___  | | __   | |  | |   ___     ___   ___ 
 | |  | | | | | | | |  / __| | |/ /   | |  | |  / _ \   / __| / __|
 | |__| | | |_| | | | | (__  |   <    | |__| | | (_) | | (__  \__ \
  \___\_\  \__,_| |_|  \___| |_|\_\   |_____/   \___/   \___| |___/
                                                                   
                                                                
	Flynet.Framework:
		:Create(InstanceName,Configuration)
			InstanceName:string
			Configuration:table ({
				'Property' = Value
			})
			Don't do local Object = :Create(), it returns table.
			Instead do local Object = :Create()()
			
			Returns Instance
			
	Framework.UI:
		:Create(InstanceName,Configuration)
			InstanceName:string -- Right now, for v1.00, this only accepts Button.
			Configuration:table ({ 
				-- This only accepts: TextScaled,BackgroundColor3,Text,TextColor3,Size,Position,Parent.
				-- However, you can use :Create().Property = Value
				Property = Value
			})
		
			Returns GuiObject
		
		:Window(PluginName)
			PluginName:string
		
			Returns GuiObject
		
		:SetWindowSettings(Window,Configuration)
			Window:GuiObject (AKA :Window())
			Configuration:table ({
			Icon = String (rbxasset/rbxassetid),
				Status = String
			})
		
		:WindowToggle(Window)
			Window:GuiObject (AKA :Window())
		
		:Notification(Configuration)
			Configuration:table ({	
				Title = String,
				Description = String
			})
	Framework.Other:
		:HTTP(Method,URL,Value) (Not implemented yet)
			Method:string (Get,Post)
			URL:string
			Value?:string
			
		(Note: This will prompt the user to allow HTTP Requests. (Allow Once, Allow Always, Deny))
		Please use this as this gives the user more trust to your plugin.
