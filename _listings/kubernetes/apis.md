---
name: Kubernetes
x-slug: kubernetes
description: Manage a cluster of Linux containers as a single system to accelerate
  Dev and simplify Ops. Kubernetes is an open source orchestration system for Docker
  containers. It handles scheduling onto nodes in a compute cluster and actively manages
  workloads to ensure that their state matches the users declared intentions. Using
  the concepts of labels and pods, it groups the containers which make up an application
  into logical units for easy management and discovery.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Name
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apis.md
specificationVersion: "0.14"
apis:
- name: Kubernetes Get Namespaces
  x-api-slug: kubernetes
  description: List objects of kind namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces
  tags: Namespaces
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespaces-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespaces-get-openapi.md
- name: Kubernetes Post Namespaces
  x-api-slug: kubernetes
  description: Create a namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces
  tags: Namespaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespaces-post-openapi.md
- name: Kubernetes Post Namespaces Bindings
  x-api-slug: kubernetes
  description: Create a binding.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/bindings
  tags: Namespaces,Bindings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesbindings-post-openapi.md
- name: Kubernetes Get Namespaces Endpoints
  x-api-slug: kubernetes
  description: List objects of kind endpoints.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/endpoints
  tags: Namespaces,Endpoints
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesendpoints-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesendpoints-get-openapi.md
- name: Kubernetes Post Namespaces Endpoints
  x-api-slug: kubernetes
  description: Create a endpoints.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/endpoints
  tags: Namespaces,Endpoints
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesendpoints-post-openapi.md
- name: Kubernetes Get Namespaces Endpoints Name
  x-api-slug: kubernetes
  description: Read the specified endpoints.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/endpoints/{name}
  tags: Namespaces,Endpoints,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesendpointsname-get-openapi.md
- name: Kubernetes Put Namespaces Endpoints Name
  x-api-slug: kubernetes
  description: Update the specified endpoints.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/endpoints/{name}
  tags: Namespaces,Endpoints,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesendpointsname-put-openapi.md
- name: Kubernetes Get Namespaces Events
  x-api-slug: kubernetes
  description: List objects of kind event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/events
  tags: Namespaces,Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesevents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesevents-get-openapi.md
- name: Kubernetes Post Namespaces Events
  x-api-slug: kubernetes
  description: Create a event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/events
  tags: Namespaces,Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesevents-post-openapi.md
- name: Kubernetes Delete Namespaces Events Name
  x-api-slug: kubernetes
  description: Delete a event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/events/{name}
  tags: Namespaces,Events,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceseventsname-delete-openapi.md
- name: Kubernetes Get Namespaces Events Name
  x-api-slug: kubernetes
  description: Read the specified event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/events/{name}
  tags: Namespaces,Events,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceseventsname-get-openapi.md
- name: Kubernetes Put Namespaces Events Name
  x-api-slug: kubernetes
  description: Update the specified event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/events/{name}
  tags: Namespaces,Events,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceseventsname-put-openapi.md
- name: Kubernetes Get Namespaces Limitranges
  x-api-slug: kubernetes
  description: List objects of kind limitrange.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/limitranges
  tags: Namespaces,Limitranges
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceslimitranges-get-openapi.md
- name: Kubernetes Post Namespaces Limitranges
  x-api-slug: kubernetes
  description: Create a limitrange.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/limitranges
  tags: Namespaces,Limitranges
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceslimitranges-post-openapi.md
- name: Kubernetes Delete Namespaces Limitranges Name
  x-api-slug: kubernetes
  description: Delete a limitrange.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/limitranges/{name}
  tags: Namespaces,Limitranges,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceslimitrangesname-delete-openapi.md
- name: Kubernetes Get Namespaces Limitranges Name
  x-api-slug: kubernetes
  description: Read the specified limitrange.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/limitranges/{name}
  tags: Namespaces,Limitranges,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceslimitrangesname-get-openapi.md
- name: Kubernetes Put Namespaces Limitranges Name
  x-api-slug: kubernetes
  description: Update the specified limitrange.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/limitranges/{name}
  tags: Namespaces,Limitranges,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespaceslimitrangesname-put-openapi.md
- name: Kubernetes Get Namespaces Pods
  x-api-slug: kubernetes
  description: List objects of kind pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/pods
  tags: Namespaces,Pods
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacespods-get-openapi.md
- name: Kubernetes Post Namespaces Pods
  x-api-slug: kubernetes
  description: Create a pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/pods
  tags: Namespaces,Pods
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacespods-post-openapi.md
- name: Kubernetes Delete Namespaces Pods Name
  x-api-slug: kubernetes
  description: Delete a pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/pods/{name}
  tags: Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacespodsname-delete-openapi.md
- name: Kubernetes Get Namespaces Pods Name
  x-api-slug: kubernetes
  description: Read the specified pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/pods/{name}
  tags: Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacespodsname-get-openapi.md
- name: Kubernetes Put Namespaces Pods Name
  x-api-slug: kubernetes
  description: Update the specified pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/pods/{name}
  tags: Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacespodsname-put-openapi.md
- name: Kubernetes Get Namespaces Replicationcontrollers
  x-api-slug: kubernetes
  description: List objects of kind replicationcontroller.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/replicationcontrollers
  tags: Namespaces,Replicationcontrollers
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesreplicationcontrollers-get-openapi.md
- name: Kubernetes Post Namespaces Replicationcontrollers
  x-api-slug: kubernetes
  description: Create a replicationcontroller.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/replicationcontrollers
  tags: Namespaces,Replicationcontrollers
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesreplicationcontrollers-post-openapi.md
- name: Kubernetes Delete Namespaces Replicationcontrollers Name
  x-api-slug: kubernetes
  description: Delete a replicationcontroller.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/replicationcontrollers/{name}
  tags: Namespaces,Replicationcontrollers,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesreplicationcontrollersname-delete-openapi.md
- name: Kubernetes Get Namespaces Replicationcontrollers Name
  x-api-slug: kubernetes
  description: Read the specified replicationcontroller.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/replicationcontrollers/{name}
  tags: Namespaces,Replicationcontrollers,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesreplicationcontrollersname-get-openapi.md
- name: Kubernetes Put Namespaces Replicationcontrollers Name
  x-api-slug: kubernetes
  description: Update the specified replicationcontroller.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/replicationcontrollers/{name}
  tags: Namespaces,Replicationcontrollers,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesreplicationcontrollersname-put-openapi.md
- name: Kubernetes Get Namespaces Resourcequotas
  x-api-slug: kubernetes
  description: List objects of kind resourcequota.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/resourcequotas
  tags: Namespaces,Resourcequotas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesresourcequotas-get-openapi.md
- name: Kubernetes Post Namespaces Resourcequotas
  x-api-slug: kubernetes
  description: Create a resourcequota.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/resourcequotas
  tags: Namespaces,Resourcequotas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesresourcequotas-post-openapi.md
- name: Kubernetes Delete Namespaces Resourcequotas Name
  x-api-slug: kubernetes
  description: Delete a resourcequota.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/resourcequotas/{name}
  tags: Namespaces,Resourcequotas,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesresourcequotasname-delete-openapi.md
- name: Kubernetes Get Namespaces Resourcequotas Name
  x-api-slug: kubernetes
  description: Read the specified resourcequota.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/resourcequotas/{name}
  tags: Namespaces,Resourcequotas,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesresourcequotasname-get-openapi.md
- name: Kubernetes Put Namespaces Resourcequotas Name
  x-api-slug: kubernetes
  description: Update the specified resourcequota.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/resourcequotas/{name}
  tags: Namespaces,Resourcequotas,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesresourcequotasname-put-openapi.md
- name: Kubernetes Post Namespaces Resourcequotausages
  x-api-slug: kubernetes
  description: Create a resourcequotausage.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/resourcequotausages
  tags: Namespaces,Resourcequotausages
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesresourcequotausages-post-openapi.md
- name: Kubernetes Get Namespaces Secrets
  x-api-slug: kubernetes
  description: List objects of kind secret.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/secrets
  tags: Namespaces,Secrets
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacessecrets-get-openapi.md
- name: Kubernetes Post Namespaces Secrets
  x-api-slug: kubernetes
  description: Create a secret.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/secrets
  tags: Namespaces,Secrets
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacessecrets-post-openapi.md
- name: Kubernetes Delete Namespaces Secrets Name
  x-api-slug: kubernetes
  description: Delete a secret.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/secrets/{name}
  tags: Namespaces,Secrets,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacessecretsname-delete-openapi.md
- name: Kubernetes Get Namespaces Secrets Name
  x-api-slug: kubernetes
  description: Read the specified secret.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/secrets/{name}
  tags: Namespaces,Secrets,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacessecretsname-get-openapi.md
- name: Kubernetes Put Namespaces Secrets Name
  x-api-slug: kubernetes
  description: Update the specified secret.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/secrets/{name}
  tags: Namespaces,Secrets,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacessecretsname-put-openapi.md
- name: Kubernetes Get Namespaces Services
  x-api-slug: kubernetes
  description: List objects of kind service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/services
  tags: Namespaces,Services
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesservices-get-openapi.md
- name: Kubernetes Post Namespaces Services
  x-api-slug: kubernetes
  description: Create a service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/services
  tags: Namespaces,Services
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesservices-post-openapi.md
- name: Kubernetes Delete Namespaces Services Name
  x-api-slug: kubernetes
  description: Delete a service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/services/{name}
  tags: Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesservicesname-delete-openapi.md
- name: Kubernetes Get Namespaces Services Name
  x-api-slug: kubernetes
  description: Read the specified service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/services/{name}
  tags: Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesservicesname-get-openapi.md
- name: Kubernetes Put Namespaces Services Name
  x-api-slug: kubernetes
  description: Update the specified service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{namespaces}/services/{name}
  tags: Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesnamespacesservicesname-put-openapi.md
- name: Kubernetes Delete Namespaces Name
  x-api-slug: kubernetes
  description: Delete a namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{name}
  tags: Namespaces,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesname-delete-openapi.md
- name: Kubernetes Get Namespaces Name
  x-api-slug: kubernetes
  description: Read the specified namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{name}
  tags: Namespaces,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesname-get-openapi.md
- name: Kubernetes Put Namespaces Name
  x-api-slug: kubernetes
  description: Update the specified namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/namespaces/{name}
  tags: Namespaces,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3namespacesname-put-openapi.md
- name: Kubernetes Delete Nodes Name
  x-api-slug: kubernetes
  description: Delete a node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/nodes/{name}
  tags: Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3nodesname-delete-openapi.md
- name: Kubernetes Get Nodes Name
  x-api-slug: kubernetes
  description: Read the specified node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/nodes/{name}
  tags: Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3nodesname-get-openapi.md
- name: Kubernetes Put Nodes Name
  x-api-slug: kubernetes
  description: Update the specified node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/nodes/{name}
  tags: Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3nodesname-put-openapi.md
- name: Kubernetes Delete Proxy Namespaces Pods Name
  x-api-slug: kubernetes
  description: Proxy delete requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}
  tags: Proxy,Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsname-delete-openapi.md
- name: Kubernetes Get Proxy Namespaces Pods Name
  x-api-slug: kubernetes
  description: Proxy get requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}
  tags: Proxy,Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsname-get-openapi.md
- name: Kubernetes Post Proxy Namespaces Pods Name
  x-api-slug: kubernetes
  description: Proxy post requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}
  tags: Proxy,Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsname-post-openapi.md
- name: Kubernetes Put Proxy Namespaces Pods Name
  x-api-slug: kubernetes
  description: Proxy put requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}
  tags: Proxy,Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsname-put-openapi.md
- name: Kubernetes Delete Proxy Namespaces Pods Name Path *
  x-api-slug: kubernetes
  description: Proxy delete requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}/{path:*}
  tags: Proxy,Namespaces,Pods,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsnamepath-delete-openapi.md
- name: Kubernetes Get Proxy Namespaces Pods Name Path *
  x-api-slug: kubernetes
  description: Proxy get requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}/{path:*}
  tags: Proxy,Namespaces,Pods,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsnamepath-get-openapi.md
- name: Kubernetes Post Proxy Namespaces Pods Name Path *
  x-api-slug: kubernetes
  description: Proxy post requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}/{path:*}
  tags: Proxy,Namespaces,Pods,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsnamepath-post-openapi.md
- name: Kubernetes Put Proxy Namespaces Pods Name Path *
  x-api-slug: kubernetes
  description: Proxy put requests to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}/{path:*}
  tags: Proxy,Namespaces,Pods,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacespodsnamepath-put-openapi.md
- name: Kubernetes Delete Proxy Namespaces Services Name
  x-api-slug: kubernetes
  description: Proxy delete requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}
  tags: Proxy,Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesname-delete-openapi.md
- name: Kubernetes Get Proxy Namespaces Services Name
  x-api-slug: kubernetes
  description: Proxy get requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}
  tags: Proxy,Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesname-get-openapi.md
- name: Kubernetes Post Proxy Namespaces Services Name
  x-api-slug: kubernetes
  description: Proxy post requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}
  tags: Proxy,Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesname-post-openapi.md
- name: Kubernetes Put Proxy Namespaces Services Name
  x-api-slug: kubernetes
  description: Proxy put requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}
  tags: Proxy,Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesname-put-openapi.md
- name: Kubernetes Delete Proxy Namespaces Services Name Path *
  x-api-slug: kubernetes
  description: Proxy delete requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}/{path:*}
  tags: Proxy,Namespaces,Services,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesnamepath-delete-openapi.md
- name: Kubernetes Get Proxy Namespaces Services Name Path *
  x-api-slug: kubernetes
  description: Proxy get requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}/{path:*}
  tags: Proxy,Namespaces,Services,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesnamepath-get-openapi.md
- name: Kubernetes Post Proxy Namespaces Services Name Path *
  x-api-slug: kubernetes
  description: Proxy post requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}/{path:*}
  tags: Proxy,Namespaces,Services,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesnamepath-post-openapi.md
- name: Kubernetes Put Proxy Namespaces Services Name Path *
  x-api-slug: kubernetes
  description: Proxy put requests to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/namespaces/{namespaces}/services/{name}/{path:*}
  tags: Proxy,Namespaces,Services,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynamespacesnamespacesservicesnamepath-put-openapi.md
- name: Kubernetes Delete Proxy Nodes Name
  x-api-slug: kubernetes
  description: Proxy delete requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}
  tags: Proxy,Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesname-delete-openapi.md
- name: Kubernetes Get Proxy Nodes Name
  x-api-slug: kubernetes
  description: Proxy get requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}
  tags: Proxy,Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesname-get-openapi.md
- name: Kubernetes Post Proxy Nodes Name
  x-api-slug: kubernetes
  description: Proxy post requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}
  tags: Proxy,Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesname-post-openapi.md
- name: Kubernetes Put Proxy Nodes Name
  x-api-slug: kubernetes
  description: Proxy put requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}
  tags: Proxy,Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesname-put-openapi.md
- name: Kubernetes Delete Proxy Nodes Name Path *
  x-api-slug: kubernetes
  description: Proxy delete requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}/{path:*}
  tags: Proxy,Nodes,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-delete-openapi.md
- name: Kubernetes Get Proxy Nodes Name Path *
  x-api-slug: kubernetes
  description: Proxy get requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}/{path:*}
  tags: Proxy,Nodes,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-get-openapi.md
- name: Kubernetes Post Proxy Nodes Name Path *
  x-api-slug: kubernetes
  description: Proxy post requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}/{path:*}
  tags: Proxy,Nodes,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-post-openapi.md
- name: Kubernetes Put Proxy Nodes Name Path *
  x-api-slug: kubernetes
  description: Proxy put requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/proxy/nodes/{name}/{path:*}
  tags: Proxy,Nodes,Name,Path,*
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-put-openapi.md
- name: Kubernetes Get Redirect Namespaces Pods Name
  x-api-slug: kubernetes
  description: Redirect get request to pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/redirect/namespaces/{namespaces}/pods/{name}
  tags: Redirect,Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3redirectnamespacesnamespacespodsname-get-openapi.md
- name: Kubernetes Get Redirect Namespaces Services Name
  x-api-slug: kubernetes
  description: Redirect get request to service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/redirect/namespaces/{namespaces}/services/{name}
  tags: Redirect,Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3redirectnamespacesnamespacesservicesname-get-openapi.md
- name: Kubernetes Get Redirect Nodes Name
  x-api-slug: kubernetes
  description: Redirect get request to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/redirect/nodes/{name}
  tags: Redirect,Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3redirectnodesname-get-openapi.md
- name: Kubernetes Get Watch Namespaces
  x-api-slug: kubernetes
  description: Watch a list of namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces
  tags: Watch,Namespaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespaces-get-openapi.md
- name: Kubernetes Get Watch Namespaces Endpoints
  x-api-slug: kubernetes
  description: Watch a list of endpoints.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/endpoints
  tags: Watch,Namespaces,Endpoints
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesendpoints-get-openapi.md
- name: Kubernetes Get Watch Namespaces Endpoints Name
  x-api-slug: kubernetes
  description: Watch a particular endpoints.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/endpoints/{name}
  tags: Watch,Namespaces,Endpoints,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesendpointsname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Events
  x-api-slug: kubernetes
  description: Watch a list of event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/events
  tags: Watch,Namespaces,Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesevents-get-openapi.md
- name: Kubernetes Get Watch Namespaces Events Name
  x-api-slug: kubernetes
  description: Watch a particular event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/events/{name}
  tags: Watch,Namespaces,Events,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespaceseventsname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Limitranges
  x-api-slug: kubernetes
  description: Watch a list of limitrange.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/limitranges
  tags: Watch,Namespaces,Limitranges
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespaceslimitranges-get-openapi.md
- name: Kubernetes Get Watch Namespaces Limitranges Name
  x-api-slug: kubernetes
  description: Watch a particular limitrange.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/limitranges/{name}
  tags: Watch,Namespaces,Limitranges,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespaceslimitrangesname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Pods
  x-api-slug: kubernetes
  description: Watch a list of pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/pods
  tags: Watch,Namespaces,Pods
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacespods-get-openapi.md
- name: Kubernetes Get Watch Namespaces Pods Name
  x-api-slug: kubernetes
  description: Watch a particular pod.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/pods/{name}
  tags: Watch,Namespaces,Pods,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacespodsname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Replicationcontrollers
  x-api-slug: kubernetes
  description: Watch a list of replicationcontroller.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/replicationcontrollers
  tags: Watch,Namespaces,Replicationcontrollers
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesreplicationcontrollers-get-openapi.md
- name: Kubernetes Get Watch Namespaces Replicationcontrollers Name
  x-api-slug: kubernetes
  description: Watch a particular replicationcontroller.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/replicationcontrollers/{name}
  tags: Watch,Namespaces,Replicationcontrollers,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesreplicationcontrollersname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Resourcequotas
  x-api-slug: kubernetes
  description: Watch a list of resourcequota.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/resourcequotas
  tags: Watch,Namespaces,Resourcequotas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesresourcequotas-get-openapi.md
- name: Kubernetes Get Watch Namespaces Resourcequotas Name
  x-api-slug: kubernetes
  description: Watch a particular resourcequota.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/resourcequotas/{name}
  tags: Watch,Namespaces,Resourcequotas,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesresourcequotasname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Secrets
  x-api-slug: kubernetes
  description: Watch a list of secret.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/secrets
  tags: Watch,Namespaces,Secrets
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacessecrets-get-openapi.md
- name: Kubernetes Get Watch Namespaces Secrets Name
  x-api-slug: kubernetes
  description: Watch a particular secret.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/secrets/{name}
  tags: Watch,Namespaces,Secrets,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacessecretsname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Services
  x-api-slug: kubernetes
  description: Watch a list of service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/services
  tags: Watch,Namespaces,Services
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesservices-get-openapi.md
- name: Kubernetes Get Watch Namespaces Services Name
  x-api-slug: kubernetes
  description: Watch a particular service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{namespaces}/services/{name}
  tags: Watch,Namespaces,Services,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesnamespacesservicesname-get-openapi.md
- name: Kubernetes Get Watch Namespaces Name
  x-api-slug: kubernetes
  description: Watch a particular namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/namespaces/{name}
  tags: Watch,Namespaces,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnamespacesname-get-openapi.md
- name: Kubernetes Get Watch Nodes Name
  x-api-slug: kubernetes
  description: Watch a particular node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443//api/v1beta3/watch/nodes/{name}
  tags: Watch,Nodes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/apiv1beta3watchnodesname-get-openapi.md
- name: Kubernetes
  x-api-slug: kubernetes
  description: Manage a cluster of Linux containers as a single system to accelerate
    Dev and simplify Ops. Kubernetes is an open source orchestration system for Docker
    containers. It handles scheduling onto nodes in a compute cluster and actively
    manages workloads to ensure that their state matches the users declared intentions.
    Using the concepts of labels and pods, it groups the containers which make up
    an application into logical units for easy management and discovery.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/kubernetes/openapi.md
x-common:
- type: x-blog
  url: http://blog.kubernetes.io/
- type: x-blog-rss
  url: http://blog.kubernetes.io/feeds/posts/default
- type: x-github
  url: https://github.com/kubernetes
- type: x-twitter
  url: https://twitter.com/kubernetesio
- type: x-website
  url: http://kubernetes.io/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---