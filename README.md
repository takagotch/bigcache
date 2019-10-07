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
```

```
```

```
```

