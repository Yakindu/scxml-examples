# SimpleHierachy 

![image](SimpleHierachy_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="SimpleHierachy">
	<state id="main_region">
		<initial>
			<transition target="A" type="internal" >
			</transition>
		</initial>
		<state id="A">
			<transition event="Event1"  target="B">
			</transition>
		</state>
		<state id="B">
			<initial>
				<transition target="B1" type="internal" >
				</transition>
			</initial>
			<state id="B1">
			</state>
		</state>
	</state>
</scxml>
```
