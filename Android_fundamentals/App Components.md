A modern android app contains many parts that can be called individually in any order and can work as standalones. Different app-components are:
1. Activities
2. Fragments
3. Services
4. Content-Providers
5. Broadcast-Receivers

App state should not be maintained in these app components as they are not sequential or constant in nature, An app can be stated from  any component based on the situation in order to handle this we follow certain architectural principles:
1. Separation of concern 
2. Drive UI from Data models
3. Single Source of Truth
4. Unidirectional Data Flow

Modern App Architecture is spilt into three layers

![[Pasted image 20241222144838.png]]
