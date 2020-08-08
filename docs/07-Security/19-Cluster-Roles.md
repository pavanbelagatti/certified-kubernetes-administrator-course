# Cluster Roles
  - Take me to [Video Tutorial](https://kodekloud.com/courses/539883/lectures/9808263)
  
In this section, we will take a look at cluster roles

## Roles
- Roles and Rolebindings are namespaced meaning they are created within namespaces.
  
  ![roles](../../images/roles.PNG)
  
## Namespaces
- Can you group or isolate nodes within  a namespace?
  - No, those are cluster wide or cluster scoped resources. They cannot be associated to any particular namespace.
  
  ![namespace](../../images/namespace.PNG)
  
- So the resources are categorized as either namespaced or cluster scoped.
  
- To see namespaced resources
  ```
  $ kubectl api-resources --namespaced=true
  ```
- To see non-namespaced resources
  ```
  $ $ kubectl api-resources --namespaced=false
  ```
  
  ![namespace1](../../images/namespace1.PNG)
  
## Cluster Roles and Cluster Role Bindings
- Cluster Roles are roles except they are for a cluster scoped resources. Kind as **`CLusterRole`** 
- The resources are nodes then create the cluster role
- The cluster role binding object links the user.
- Create a cluster role or cluster role binding with kubectl command
  ```
  $ kubectl create -f cluster-admin-role.yaml
  $ kubectl create -f cluster-admin-role-binding.yaml
  ```
  
  ![cr](../../images/cr.PNG)
  
- You can create a cluster role for namespace resources as well. When you do that user will have access to these resources across all namespaces.
- 
  
  