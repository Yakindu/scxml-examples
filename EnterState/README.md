# EnterState 

![image](EnterState_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="EnterState">
	<state id="r">
		<initial>
			<transition target="A" type="internal" >
			</transition>
		</initial>
		<state id="A">
			<transition event="e"  target="B">
			</transition>
			<transition event="f"  target="F">
			</transition>
			<transition event="g"  target="E">
			</transition>
		</state>
		<state id="B">
			<initial>
				<transition target="E" type="internal" >
				</transition>
			</initial>
			<state id="E">
			</state>
			<state id="F">
			</state>
		</state>
	</state>
</scxml>
```
