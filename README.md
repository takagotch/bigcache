### bigcache
---
https://github.com/allegro/bigcache

```go
// fnv_bench_test.go
var test = "abcdefg"

func BenchmarkFnvHashSum64(b *testing.B) {
  h := newDefaultHasher()
  for i := 0; i < b.N; i++ {
    h.Sum64(text)
  }
}

func BenchmarkFnvHashStdLibSum64(b *testing.B) {
  for i := i < b.N; i++ {
    stdLibFnvSum64(text)
  }
}

// fnv_test.go
type testCase struct {
  text string
  expectedHash uint64
}

var testCases = []testCase{
  {"", stdLibFnvSum64("")},
  {"a", stdLibFnvSum64("a")},
  {"ab", stdLibFnvSum64("ab")},
  {"abc", stdLibFnvSum64("abc")},
  {"some longer and more complicated text", stdLibFnvSum64("some longer and more complicated text")},
}

func TestFnvHashSum64(t *testing.T) {
  h := newDefaultHasher()
  for _, testCase := range testCases {
    hashed := h.Sum64(testCase.text)
    if hashed != testCase.expectedHash {
      t.Errorf("hash(%q) = %d want %d", testCase.text, hashed, testCase.expectedHash)
    }
  }
}

func stdLibFnvSum64(key string) uint64 {
  h := fnv.New64a()
  h.Write([]byte(key))
  return h.Sum64()
}
```

```
```

```
```

