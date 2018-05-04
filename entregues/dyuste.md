
# VERSIÓ DEFINITIVA

Agafarem el dau sempre que sigui 3 o més gran.

```
create function dbo.mElsQuedo( @nJugador  int, @punts  int ) 
returns bit
as begin 
	declare @meloquedo as bit 
	if @punts >=2
		set @meloquedo = 1
	else 
		set @meloquedo =0
	return @meloquedo
end

```
