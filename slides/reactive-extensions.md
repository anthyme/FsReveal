- title : Reactive Extensions
- description : Reactive Extensions
- author : Anthyme Caillard
- theme : Sky
- transition : default

***

# Reactive Extensions

---

## Visiteur, qui es-tu ?

- Qui connait async/await, Task ?
- Qui connait Observable ?
- Qui connait Rx ?

---

```csharp
button.Click += (s, args) => {
    if (something){
        // raise another event
    }
}

button.Click -= /* ???? */

```

' Event based ?
' Not composable
' 

***





# IEnumerable

# VS

# IObservable


---


```csharp
interface IEnumerable<out T> 
{
    IEnumerator<T> GetEnumerator();
}
```

```csharp
interface IEnumerator<in T> 
{
    void MoveNext();
    T Current { get; }
    void Reset();
}
```

---


```csharp
interface IObservable<out T> 
{
    IDisposable Subscribe(IObserver<T> observer);
}
```

```csharp
interface IObserver<in T> 
{
    void OnCompleted();
    void OnNext(T value);
    void OnError(Exception error);
}
```

---

![enumerable-observable](images/reactive-extensions/enumerable-observable.png)


***









## Reactive Extensions

---

> Rx is a library to create and compose event based asynchronous program with observables

---

### Primitives

```csharp
Observalbe.Empty<int>()     // OnCompleted

Observalbe.Return(42)       // OnNext

Observalbe.Throw<int>(ex)   // OnError

Observalbe.Never<int>()     // Nothing ...
```


***



sources
IEnumerable
event
subjet
async code

operator
throttle
interval
delay
buffer


reduce
filter,accumulate, aggregate, partition

map
select

combine
concatenate, merge, pair

control overflow

synchronisationContext





# Observable Observer

***





### Plateformes

- Rx.Net
- RxJs
- RxJava
-


# Reactive Extensions based architecture

***
