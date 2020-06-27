# ch11_testing
Go unit test example from Donovan and Kernighan

The **go test** subcommand is a test driver for Go packages which are organised by certain conventions.  
Files whose names end in "_test.go" are not included in the package built by **go build** but are a part when built by **go test**.

The test driver will treat functions differently according to the naming convention.

Benchmark* functions will report a performance metric.

Test* functions will pass or fail a test for correct behaviour.

Example* functions provide machine checked documentation.

```
import "testing"
func TestPalindrome(t *testing.T) { /* etc */ }
```

**go test** runs all tests.  
**go test -v --run="French|Canal"** runs tests where the function names matches the regex pattern. -v is verbose output
