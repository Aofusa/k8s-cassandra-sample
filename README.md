Kubernetes Cassandra Sample
=====


Kubernetes 上で Cassandra を動作させてみるサンプル  


- クラスタの起動

```sh
kubectl apply -f .
```


- クラスタに対してクエリを実行する

```sh
kubectl run cassandra-csql \
    --rm \
    --image=cassandra \
    --restart=Never \
    -i --tty \
    --command -- cqlsh sample-cassandra
```


- クラスタの削除

```sh
kubectl delete -f .
```
