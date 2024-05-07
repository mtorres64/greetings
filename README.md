# Saludos en go

Este paquete prporciona una forma simple de obtener saludos personalizados en GO

## Instalacion
Ejecuta el siguiente comando para instalar el paquete:
```bash
go get -u github.com/MarceloTorres06/greetings
```

## Uso
Aqui tienes un ejemplo de uso del paquete:

```go
package main

import (
	"fmt"
	"log"

	"github.com/MarceloTorres06/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	names := []string{
		"Marcelo",
		"Raúl",
		"Nicolás",
	}

	saludos, err := greetings.Hellos(names)

	if err != nil {
		log.Fatal(err)
	}

	fmt.Println(saludos)

}
```