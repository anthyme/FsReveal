- title : Tacler la complexité avec Event Sourcing et CQRS
- description : Tacler la complexité avec Event Sourcing et CQRS
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

> Rx is a library to create and compose event based asynchronous program with observables

---

```csharp
button.Click += (s, args) => {
    if (something){
        // raise another event
    }
}

button.Click -= /* ???? */

```

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

***







# Observable Observer

***








# Observable Observer

***
