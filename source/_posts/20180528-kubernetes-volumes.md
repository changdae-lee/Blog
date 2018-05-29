---
title: kubernetes_volumes
tags:
  - kubernetes
  - storage
categories:
  - Infrastructure
  - Kubernetes
date: 2018-05-28 19:48:44
---

* pod의 component
* standlone object가 아님.
* access하고 싶으면 container에 마운트 해주어야 함.

## Volume types
* emptyDir: 일시적인 데이터를 저장하는 단순 empty 디렉토리
* hostPath: worker 노드의 파일 시스템의 디렉토리를 pod에 마운팅시킬 때 사용
* gitRepo:
* nfs
* gcePersistentDisk, awsElasticBlockStore, azureDisk
* cinder, cephfs, iscsi, flocker, glusterfs, quobyte, rbd, flexVolume, vsphereVolume, photonPersistentDisk, scaleIO: 여러 종류의 네트워크 스토리지를 마운트시킬 때
* configMap, secret, downwardAPI: 쿠버네티스 자원과 클러스터 정보를 포드로 노출시킬 때
* persistentVolumeClaim: preprovision되거나 dynamic하게 provisioning할 수 있는 영구 스토리지
