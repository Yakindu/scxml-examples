# RaiseEvent 

![image](RaiseEvent_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="RaiseEvent">
	<parallel>
	<state id="main_region">
		<initial>
			<transition target="StateA" type="internal" >
			</transition>
		</initial>
		<state id="StateA">
			<transition event="e2"  target="StateB">
			</transition>
		</state>
		<state id="StateB">
			<onentry>
				<send event="e1">
				</send>
			</onentry>
		</state>
	</state>
	<state id="second_region">
		<initial>
			<transition target="StateA1" type="internal" >
			</transition>
		</initial>
		<state id="StateA1">
			<transition event="e1"  target="StateB1">
			</transition>
		</state>
		<state id="StateB1">
		</state>
	</state>
	</parallel>
</scxml>
```
