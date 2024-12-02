A ViewModel is always created in association with a scope (a fragment or an activity) and will be retained as long as the scope is alive. E.g. if it is an Activity, until it is finished. In other words, this means that a ViewModel will not be destroyed if its owner is destroyed for a configuration change (e.g. rotation). The new owner instance just re-connects to the existing model.

### **Key Classes Involved**
1. **`ViewModelStore`**:
    - A simple map (`HashMap<String, ViewModel>`) that holds `ViewModel` instances, keyed by their names or types.
    - Responsible for retaining and clearing `ViewModel` instances.
    - It is tied to the Scope (Activity or fragment)
1. **`ViewModelProvider`**:
    - Provides access to the `ViewModel` instances stored in the `ViewModelStore`.
    - Uses a `ViewModelProvider.Factory` to create new instances when needed.
2. **`ViewModelProvider.Factory`**:
    - Interface to define how new `ViewModel` instances are created.
    - By default, it uses `DefaultViewModelProviderFactory`, but you can define custom factories for injecting dependencies.