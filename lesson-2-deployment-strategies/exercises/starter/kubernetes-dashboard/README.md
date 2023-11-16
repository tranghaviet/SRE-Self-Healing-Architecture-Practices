Follow https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md to get token

```
kubectl apply -f long-term.yml
# or
# kubectl apply -f short-term.yml
kubectl apply -f r.yml
# long term token
kubectl get secret admin-user -n kubernetes-dashboard -o jsonpath={".data.token"} | base64 -d
# short term token
kubectl -n kubernetes-dashboard create token admin-user
```
