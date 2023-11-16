Follow https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md to get token

```
kubectl apply -f s.yml
kubectl apply -f r.yml
kubectl get secret admin-user -n kubernetes-dashboard -o jsonpath={".data.token"} | base64 -d
```
