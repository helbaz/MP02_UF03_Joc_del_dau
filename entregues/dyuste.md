
# VERSIÓ DEFINITIVA

Agafarem el dau sempre que sigui 3 o més gran.

```


create function melsquedo(@jugador as int, @punts as int)
returns bit
as begin

	declare @melosquedo as bit, @yo as int, @el as int;
	set @yo=(select sum(puntsAnotats) from marcador where nJugadorAnota=@jugador)
	set @el=(select sum(puntsAnotats) from marcador where nJugadorAnota!=@jugador)
	
	if @punts>=3
		if @yo>@el
			set @melosquedo=1;
		else	 
			set @melosquedo=1;
	else if @punts < =2

		if @yo<@el
			set @melosquedo=1;
		else
			set @melosquedo=0;

	return @melosquedo
end



```
