# ExitState 

![image](ExitState_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="ExitState">
	<state id="r">
		<initial>
			<transition target="A" type="internal" >
			</transition>
		</initial>
		<state id="A">
			<initial>
				<transition target="B" type="internal" >
				</transition>
			</initial>
			<state id="B">
				<transition event="g"  target="E">
				</transition>
				<transition event="f"  target="F">
				</transition>
				<transition event="e"  target="E">
				</transition>
			</state>
		</state>
		<state id="E">
		</state>
		<state id="F">
		</state>
	</state>
</scxml>
```
