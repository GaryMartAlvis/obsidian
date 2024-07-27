```dax
// Buscarv con rango abierto
=
var plazo = [plazo_dpf]
return
CALCULATE(
	MAX(tRangoMN[RANGO]),
	FILTER(
	             tRangoMN,
	             plazo <= tRangoMN[HASTA:] && plazo >= tRangoMN[DE:]
	 )
)
```

```dax
// Cumplimiento de multiples condiciones (OR, AND)
=
var plazo = [plazo_dpf]
var tasa  = [tasa_contratada]
return
IF(
	(plazo = 450 && tasa = 6.5) || (plazo = 540 && tasa = 7),
	TRUE(),
	FALSE()
)
```


