# Saludos en Go

Este paquete proporciona una forma simple de obtener saludos personalizados.

## Instalación

Ejecuta el siguiente comando para instalar el paquete:

```bash
go get -u github.com/Joselm1234/greetings
```

## Uso

Aquí tienes un ejemplo de como utilizar el paquete en tu codigo:

```go
package main

import (
    "fmt"
    "github.com/Joselm1234/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	names := []string{"Jose", "Pedro", "Juan"}
	messages, err := greetings.Hellos(names)
    if err != nil {
		log.Fatal(err)
	}
	message, err := greetings.Hello("Jose Luis")
	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(messages)
    fmt.Println(message)
}
```
