* kube-controllermanager
    * a sort of office with different resp monitoring and adapt
    * actions:
        * watch status
        * remediate situation
    * a component that watches always the state of various components of the system and work to whole system to a desidered state

* node-controller: resp monitoring nodes with kube-apiserver 
    * `NODE_MONITOR_PERIOD` every 5 seconds
    * `NODE_MONITOR_GRACE_PERIOD` every 40s (prima di etichettarla come `UNREACHBLE`)
    * se viene etichettata come `UNREACHBLE` ha `POD_EVICTED_TIMEOUT` 5min (se si superano i 5m i pod vengono spostati sui node sani [se fanno parte di un ReplicaSet])

* replication-controller: resp monitoring replicaset e garantire sempre il numero di pod desiderato all'interno del set. Se un pod termina viene creato un altro. 

* ci sono altri controller:
    * namespace controller
    * deployment controller
    * serviceaccount controller
    * etc.

* where are set? in Kubernetes Controller Mager

