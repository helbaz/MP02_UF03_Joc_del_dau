
# VERSIÓ DEFINITIVA

Agafarem el dau sempre que sigui 3 o més gran.

```


alter function melsquedo(@jugador as int, @punts as int)
returns bit
as begin

	declare @melosquedo as bit, @yo as int, @el as int;
	set @yo=coalesce((select sum(puntsAnotats) from marcador where nJugadorAnota=@jugador),0);
	set @el=coalesce((select sum(puntsAnotats) from marcador where nJugadorAnota!=@jugador),0);
	
	if @punts>=3
		begin
			if @yo>@el
				set @melosquedo=1;
			else 
				set  @melosquedo=1;
		end
	else if @punts < =2
		begin
			if @yo<@el
				set @melosquedo=1;
			else 
				set @melosquedo=0;
			end
	return @melosquedo
end







```
