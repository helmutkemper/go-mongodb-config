# go-mongodb-config
A package for reading/writing MongoDB yaml-based configurations

## Usage
Create 'Config' from file:
```
import "github.com/timvaillancourt/go-mongodb-config/config"

func main() {
	config, err := config.ReadConfig("/etc/mongod.conf")
	if err != nil {
		panic(err)
	}
	...
}
```

Write 'Config' to file:

```
import "github.com/timvaillancourt/go-mongodb-config/config"
 
func main() {
	config := &config.Config{}
	...
	err := config.Write("/etc/mongod.conf")
	if err != nil {
		panic(err)
	}
}
```
