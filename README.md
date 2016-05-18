# Pooly

An example from [The Little Elixir & OPT Guidebook](https://www.manning.com/books/the-little-elixir-and-otp-guidebook) by Benjamin Tan Wei Hao.

https://github.com/benjamintanweihao/the-little-elixir-otp-guidebook-code


```bash
iex -S mix
```

Once you are inside iex, try following:
```
> :observer.start
> Pooly.status("Pool1")
> w1 = Pooly.checkout("Pool1")
> w2 = Pooly.checkout("Pool1")
> w3 = Pooly.checkout("Pool1")
> SampleWorker.work_for(w3, 20000) # wait for 20 seconds
> w4 = Pooly.checkout("Pool1", true, :infinity) # wait until any worker is available
```
