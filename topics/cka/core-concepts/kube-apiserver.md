* you can use http api request instead POST
    1. authenticate user
    2. validate request
    3. retrieve data
    4. update ETCD
    5. scheduler
    6. kubelet

* kube-apiserver
    * authenticate
    * convalidate
    * keep info from ETCD and update/insert data in ETCD
    * only component that interact directly with ETCD
