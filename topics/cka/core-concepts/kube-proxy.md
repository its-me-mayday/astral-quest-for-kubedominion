* kube-proxy
    * pod => internal virtual network
    * comunicazione tra podi di differenti nodi => no podip ma c'è un service per comnuicare
    * service accesibile in tutto il nodo => kube proxy è il processo che viene eseguito su ogni nodo e cerca nuovi servizi quando ne vengono creati nuovi e gestisce il traffico verso gli stessi
