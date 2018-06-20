{
  "info": {
    "name": "AWS OpsWorks API Get Hostname Suggestion",
    "_postman_id": "d5a97337-c311-4962-baf0-c688a698297f",
    "description": "Gets a generated host name for the specified layer, based on the current host name theme.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Instances",
      "item": [
        {
          "id": "1c201acb-9496-4164-a97f-91aa9e3da5b4",
          "name": "assignInstance",
          "request": {
            "url": "http://example.com/api/?Action=AssignInstance?InstanceId=InstanceId&LayerIds=LayerIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Assign a registered instance to a layer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "91aef875-a42e-4535-b7af-1ab5fceaedf0"
            }
          ]
        },
        {
          "id": "f181d06d-9b61-4f67-a53b-b5d8d08e6a3d",
          "name": "createInstance",
          "request": {
            "url": "http://example.com/api/?Action=CreateInstance?AgentVersion=AgentVersion&AmiId=AmiId&Architecture=Architecture&AutoScalingType=AutoScalingType&AvailabilityZone=AvailabilityZone&BlockDeviceMappings=BlockDeviceMappings&EbsOptimized=EbsOptimized&Hostname=Hostname&InstallUpdatesOnBoot=InstallUpdatesOnBoot&InstanceType=InstanceType&LayerIds=LayerIds&Os=Os&RootDeviceType=RootDeviceType&SshKeyName=SshKeyName&StackId=StackId&SubnetId=SubnetId&Tenancy=Tenancy&VirtualizationType=VirtualizationType",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an instance in a specified stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "76aa6af8-bb3b-4f22-828f-b3ee0ebb6291"
            }
          ]
        },
        {
          "id": "a694e581-4459-403a-84ff-d8081c689285",
          "name": "deleteInstance",
          "request": {
            "url": "http://example.com/api/?Action=DeleteInstance?DeleteElasticIp=DeleteElasticIp&DeleteVolumes=DeleteVolumes&InstanceId=InstanceId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a specified instance, which terminates the associated Amazon EC2 instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "587a6cb1-cc16-4e37-bb8d-792c40cb2700"
            }
          ]
        },
        {
          "id": "c8d92c8d-fd51-4593-90a5-261546c5f477",
          "name": "deregisterInstance",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterInstance?InstanceId=InstanceId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deregister a registered Amazon EC2 or on-premises instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "913ee237-8985-47cc-bfc8-964645f54d73"
            }
          ]
        },
        {
          "id": "254a7a1a-4b03-421c-8ceb-23406d640eef",
          "name": "deregisterRdsDbInstance",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterRdsDbInstance?RdsDbInstanceArn=RdsDbInstanceArn",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deregisters an Amazon RDS instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a4c3941a-3fb3-4112-b34a-6a6a61e5fe9d"
            }
          ]
        },
        {
          "id": "00f73dc1-2535-42e2-bacf-566dfe5bbd11",
          "name": "describeInstances",
          "request": {
            "url": "http://example.com/api/?Action=DescribeInstances?InstanceIds=InstanceIds&LayerId=LayerId&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Requests a description of a set of instances."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c89bd3f-6f79-4456-8a44-eb1ec5e1d08b"
            }
          ]
        },
        {
          "id": "951ca188-0fb7-4b01-abac-e74ef25f1d65",
          "name": "describeRdsDbInstances",
          "request": {
            "url": "http://example.com/api/?Action=DescribeRdsDbInstances?RdsDbInstanceArns=RdsDbInstanceArns&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes Amazon RDS instances."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "71eef70b-a918-4bc1-bc7f-87afc8a17b18"
            }
          ]
        }
      ]
    },
    {
      "name": "Volumes",
      "item": [
        {
          "id": "1fd62aa1-178f-433b-9fa0-cc79f3ba4749",
          "name": "assignVolume",
          "request": {
            "url": "http://example.com/api/?Action=AssignVolume?InstanceId=InstanceId&VolumeId=VolumeId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Assigns one of the stack's registered Amazon EBS volumes to a specified instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b1412b16-226e-4bd3-8322-cd63d81d485b"
            }
          ]
        },
        {
          "id": "28ec57d5-f6ea-45da-b129-7dce4a547dbd",
          "name": "deregisterVolume",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterVolume?VolumeId=VolumeId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deregisters an Amazon EBS volume."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c0134cab-7616-4d09-81ec-b4a7a0919341"
            }
          ]
        },
        {
          "id": "784c41fe-d72f-4569-b1c8-a151edcd0c25",
          "name": "describeVolumes",
          "request": {
            "url": "http://example.com/api/?Action=DescribeVolumes?InstanceId=InstanceId&RaidArrayId=RaidArrayId&StackId=StackId&VolumeIds=VolumeIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes an instance's Amazon EBS volumes."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a208796-5117-4e2f-bd90-6ea51d385058"
            }
          ]
        }
      ]
    },
    {
      "name": "IP Addresses",
      "item": [
        {
          "id": "013e352a-068a-4b74-9869-e378fb506feb",
          "name": "associateElasticIp",
          "request": {
            "url": "http://example.com/api/?Action=AssociateElasticIp?ElasticIp=ElasticIp&InstanceId=InstanceId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Associates one of the stack's registered Elastic IP addresses with a specified instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c450dd41-f8d0-4a96-93f8-d7749f17d20e"
            }
          ]
        },
        {
          "id": "6834da53-ec31-4249-ad88-c14bf5233a8e",
          "name": "deregisterElasticIp",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterElasticIp?ElasticIp=ElasticIp",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deregisters a specified Elastic IP address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e7c274f-fe4e-4548-b21a-105e5a7835e0"
            }
          ]
        },
        {
          "id": "99d7deec-449d-4393-9734-64360ac7ef30",
          "name": "describeElasticIps",
          "request": {
            "url": "http://example.com/api/?Action=DescribeElasticIps?InstanceId=InstanceId&Ips=Ips&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes Elastic IPs"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "05d19e24-c8d1-420b-83a7-5bf29e640ba0"
            }
          ]
        },
        {
          "id": "511a91dd-e2b2-47e0-98a4-4b4495268a8a",
          "name": "disassociateElasticIp",
          "request": {
            "url": "http://example.com/api/?Action=DisassociateElasticIp?ElasticIp=ElasticIp",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Disassociates an Elastic IP address from its instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ccb3be32-1f38-4ff8-8d3e-6100b216891f"
            }
          ]
        }
      ]
    },
    {
      "name": "Load Balancers",
      "item": [
        {
          "id": "59bb7815-083d-4b70-93f8-91c747c6e7cf",
          "name": "attachElasticLoadBalancer",
          "request": {
            "url": "http://example.com/api/?Action=AttachElasticLoadBalancer?ElasticLoadBalancerName=ElasticLoadBalancerName&LayerId=LayerId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Attaches an Elastic Load Balancing load balancer to a specified layer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec86b980-8d6a-4e06-8f10-a33dbe63aedc"
            }
          ]
        },
        {
          "id": "0e9dcde6-df84-4594-95ab-71ed0ea86fc6",
          "name": "describeElasticLoadBalancers",
          "request": {
            "url": "http://example.com/api/?Action=DescribeElasticLoadBalancers?LayerIds=LayerIds&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes a stack's Elastic Load Balancing instances."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b71f338-552b-477e-a85d-cc545a6190fb"
            }
          ]
        },
        {
          "id": "2321ace2-ab4d-44c9-98d3-55aeace06376",
          "name": "detachElasticLoadBalancer",
          "request": {
            "url": "http://example.com/api/?Action=DetachElasticLoadBalancer?ElasticLoadBalancerName=ElasticLoadBalancerName&LayerId=LayerId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Detaches a specified Elastic Load Balancing instance from its layer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c555240e-7f4b-4176-b3dd-29e76eae07a8"
            }
          ]
        }
      ]
    },
    {
      "name": "Stacks",
      "item": [
        {
          "id": "6dbe54ff-6711-4410-91b6-8df2230de93f",
          "name": "cloneStack",
          "request": {
            "url": "http://example.com/api/?Action=CloneStack?AgentVersion=AgentVersion&Attributes=Attributes&ChefConfiguration=ChefConfiguration&CloneAppIds=CloneAppIds&ClonePermissions=ClonePermissions&ConfigurationManager=ConfigurationManager&CustomCookbooksSource=CustomCookbooksSource&CustomJson=CustomJson&DefaultAvailabilityZone=DefaultAvailabilityZone&DefaultInstanceProfileArn=DefaultInstanceProfileArn&DefaultOs=DefaultOs&DefaultRootDeviceType=DefaultRootDeviceType&DefaultSshKeyName=DefaultSshKeyName&DefaultSubnetId=DefaultSubnetId&HostnameTheme=HostnameTheme&Name=Name&Region=Region&ServiceRoleArn=ServiceRoleArn&SourceStackId=SourceStackId&UseCustomCookbooks=UseCustomCookbooks&UseOpsworksSecurityGroups=UseOpsworksSecurityGroups&VpcId=VpcId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a clone of a specified stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9f395aca-3b99-4917-b930-89dfdb800de8"
            }
          ]
        },
        {
          "id": "b06fd465-5b3c-40a3-8cb8-6259ccf3fabf",
          "name": "describeStackProvisioningParameters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeStackProvisioningParameters?StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Requests a description of a stack's provisioning parameters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2025999b-f9c9-4ba2-a02a-2934c625bcf2"
            }
          ]
        },
        {
          "id": "08239e24-794f-4dbc-beba-2444d6b709e8",
          "name": "describeStacks",
          "request": {
            "url": "http://example.com/api/?Action=DescribeStacks?StackIds=StackIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Requests a description of one or more stacks."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "86c1fbcd-7662-4f0d-ab1c-34b5f50549f3"
            }
          ]
        },
        {
          "id": "6664dff7-e414-49fe-aea2-10b6a3074c03",
          "name": "describeStackSummary",
          "request": {
            "url": "http://example.com/api/?Action=DescribeStackSummary?StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the number of layers and apps in a specified stack, and the number of instances in\n      each state, such as running_setup or online."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b90b2009-e750-43f0-95a2-067e9d12d3a6"
            }
          ]
        }
      ]
    },
    {
      "name": "Applications",
      "item": [
        {
          "id": "a00f83dd-4684-4303-a478-047937a5b714",
          "name": "createApp",
          "request": {
            "url": "http://example.com/api/?Action=CreateApp?AppSource=AppSource&Attributes=Attributes&DataSources=DataSources&Description=Description&Domains=Domains&EnableSsl=EnableSsl&Environment=Environment&Name=Name&Shortname=Shortname&SslConfiguration=SslConfiguration&StackId=StackId&Type=Type",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an app for a specified stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "41f56dc9-4808-482e-b9ea-646e32d2f11e"
            }
          ]
        },
        {
          "id": "2236715b-8789-4abb-b363-21b4b5294e19",
          "name": "deleteApp",
          "request": {
            "url": "http://example.com/api/?Action=DeleteApp?AppId=AppId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a specified app."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "50202ace-35a5-44ae-9a29-236de2d2091e"
            }
          ]
        },
        {
          "id": "38c9c36f-18d7-4ab3-a240-3c11808f4a1b",
          "name": "describeApps",
          "request": {
            "url": "http://example.com/api/?Action=DescribeApps?AppIds=AppIds&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Requests a description of a specified set of apps."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e44e3e12-1295-40b1-8427-96b91661785e"
            }
          ]
        }
      ]
    },
    {
      "name": "Folder",
      "item": [
        {
          "id": "3ae3e759-9f9f-4426-994a-f992027ee285",
          "name": "createDeployment",
          "request": {
            "url": "http://example.com/api/?Action=CreateDeployment?AppId=AppId&Command=Command&Comment=Comment&CustomJson=CustomJson&InstanceIds=InstanceIds&LayerIds=LayerIds&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Runs deployment or stack commands."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a699152-a5a0-4016-ae87-27cd75d456a7"
            }
          ]
        },
        {
          "id": "e18923dc-7e0a-41e0-8a01-97712c00bc7d",
          "name": "createLayer",
          "request": {
            "url": "http://example.com/api/?Action=CreateLayer?Attributes=Attributes&AutoAssignElasticIps=AutoAssignElasticIps&AutoAssignPublicIps=AutoAssignPublicIps&CustomInstanceProfileArn=CustomInstanceProfileArn&CustomJson=CustomJson&CustomRecipes=CustomRecipes&CustomSecurityGroupIds=CustomSecurityGroupIds&EnableAutoHealing=EnableAutoHealing&InstallUpdatesOnBoot=InstallUpdatesOnBoot&LifecycleEventConfiguration=LifecycleEventConfiguration&Name=Name&Packages=Packages&Shortname=Shortname&StackId=StackId&Type=Type&UseEbsOptimizedInstances=UseEbsOptimizedInstances&VolumeConfigurations=VolumeConfigurations",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a layer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "258d5f7f-5e79-4d6b-8d14-bc84456893f9"
            }
          ]
        },
        {
          "id": "bc937a1f-12ce-445d-8eed-2cfd85551874",
          "name": "createStack",
          "request": {
            "url": "http://example.com/api/?Action=CreateStack?AgentVersion=AgentVersion&Attributes=Attributes&ChefConfiguration=ChefConfiguration&ConfigurationManager=ConfigurationManager&CustomCookbooksSource=CustomCookbooksSource&CustomJson=CustomJson&DefaultAvailabilityZone=DefaultAvailabilityZone&DefaultInstanceProfileArn=DefaultInstanceProfileArn&DefaultOs=DefaultOs&DefaultRootDeviceType=DefaultRootDeviceType&DefaultSshKeyName=DefaultSshKeyName&DefaultSubnetId=DefaultSubnetId&HostnameTheme=HostnameTheme&Name=Name&Region=Region&ServiceRoleArn=ServiceRoleArn&UseCustomCookbooks=UseCustomCookbooks&UseOpsworksSecurityGroups=UseOpsworksSecurityGroups&VpcId=VpcId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "53331dcc-98f7-44f9-a382-c6b4ce2f1acc"
            }
          ]
        },
        {
          "id": "08d28b0e-9988-43c2-b46c-a23cd2ba6f7e",
          "name": "createUserProfile",
          "request": {
            "url": "http://example.com/api/?Action=CreateUserProfile?AllowSelfManagement=AllowSelfManagement&IamUserArn=IamUserArn&SshPublicKey=SshPublicKey&SshUsername=SshUsername",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new user profile."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd8503ec-d50f-499c-a736-647189a0083b"
            }
          ]
        },
        {
          "id": "9ecdf8d1-7817-4fc1-a639-8ad3225c4b1d",
          "name": "deleteLayer",
          "request": {
            "url": "http://example.com/api/?Action=DeleteLayer?LayerId=LayerId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a specified layer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "175b1c44-6662-42c4-a0d4-b40862d98479"
            }
          ]
        },
        {
          "id": "b97ceb13-6170-4a25-9189-a4a3ca127a0a",
          "name": "deleteStack",
          "request": {
            "url": "http://example.com/api/?Action=DeleteStack?StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a specified stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "225db035-18d7-4462-982e-cddcc4638ce9"
            }
          ]
        },
        {
          "id": "7c7db11e-1cdc-49b7-ba2d-e3ddbef73417",
          "name": "deleteUserProfile",
          "request": {
            "url": "http://example.com/api/?Action=DeleteUserProfile?IamUserArn=IamUserArn",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a user profile."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "271a9bc6-7322-4dcf-b315-4a148e1b6f6e"
            }
          ]
        },
        {
          "id": "76ce8afb-4458-458c-b860-1bc8ad0c9724",
          "name": "deregisterEcsCluster",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterEcsCluster?EcsClusterArn=EcsClusterArn",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deregisters a specified Amazon ECS cluster from a stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57219bf9-65da-4a51-949c-6910c932dc38"
            }
          ]
        }
      ]
    },
    {
      "name": "Agent Versions",
      "item": [
        {
          "id": "e8f4f568-ede5-48ab-97fb-f80072963054",
          "name": "describeAgentVersions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeAgentVersions?ConfigurationManager=ConfigurationManager&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the available AWS OpsWorks Stacks agent versions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1251030f-887a-429f-bbee-c926dc944559"
            }
          ]
        }
      ]
    },
    {
      "name": "Commands",
      "item": [
        {
          "id": "2055efd6-2a4a-4b60-9e5b-74ff3d1c18c8",
          "name": "describeCommands",
          "request": {
            "url": "http://example.com/api/?Action=DescribeCommands?CommandIds=CommandIds&DeploymentId=DeploymentId&InstanceId=InstanceId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the results of specified commands."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6364d635-62c8-483d-b9b0-4d7fcdcd59d4"
            }
          ]
        }
      ]
    },
    {
      "name": "Deployments",
      "item": [
        {
          "id": "2edab9d9-5faf-466b-974b-a8b4afcbd140",
          "name": "describeDeployments",
          "request": {
            "url": "http://example.com/api/?Action=DescribeDeployments?AppId=AppId&DeploymentIds=DeploymentIds&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Requests a description of a specified set of deployments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "20045419-5a48-4fda-b917-c4e45045c355"
            }
          ]
        }
      ]
    },
    {
      "name": "ECS Clusters",
      "item": [
        {
          "id": "46bb3b66-8486-44f3-a516-ed697ba15dcb",
          "name": "describeEcsClusters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEcsClusters?EcsClusterArns=EcsClusterArns&MaxResults=MaxResults&NextToken=NextToken&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes Amazon ECS clusters that are registered with a stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9277b7a4-2c33-4e06-9670-e8054ae524d0"
            }
          ]
        }
      ]
    },
    {
      "name": "Layers",
      "item": [
        {
          "id": "7479d2a8-92b8-41dd-9d74-8fc65157ff7e",
          "name": "describeLayers",
          "request": {
            "url": "http://example.com/api/?Action=DescribeLayers?LayerIds=LayerIds&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Requests a description of one or more layers in a specified stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "44ae7859-54e0-4835-9f49-0516834bcc02"
            }
          ]
        }
      ]
    },
    {
      "name": "Auto Scaling",
      "item": [
        {
          "id": "7f53b457-86be-4199-8a1e-785e7e601369",
          "name": "describeLoadBasedAutoScaling",
          "request": {
            "url": "http://example.com/api/?Action=DescribeLoadBasedAutoScaling?LayerIds=LayerIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes load-based auto scaling configurations for specified layers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e821e15c-60d0-4326-98bf-dfe3fbc99378"
            }
          ]
        },
        {
          "id": "4fc05699-1229-4412-8794-1ab67b16e37b",
          "name": "describeTimeBasedAutoScaling",
          "request": {
            "url": "http://example.com/api/?Action=DescribeTimeBasedAutoScaling?InstanceIds=InstanceIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes time-based auto scaling configurations for specified instances."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "09642015-90f0-4541-b51d-7f7dcccdaaf6"
            }
          ]
        }
      ]
    },
    {
      "name": "Users",
      "item": [
        {
          "id": "eff08705-a770-403d-b149-bcb9e9f88847",
          "name": "describeMyUserProfile",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMyUserProfile?UserProfile=UserProfile",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes a user's SSH information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ae9bd35a-9935-4c0f-8c0e-e638bd55353f"
            }
          ]
        },
        {
          "id": "689303b7-532a-460e-8b24-b4eac50f7821",
          "name": "describeUserProfiles",
          "request": {
            "url": "http://example.com/api/?Action=DescribeUserProfiles?IamUserArns=IamUserArns",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describe specified users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "51227752-93dc-4404-8a91-86062ceabdd9"
            }
          ]
        }
      ]
    },
    {
      "name": "Permissions",
      "item": [
        {
          "id": "4298eaac-492d-4de9-b9ef-bab112d1f5d7",
          "name": "describePermissions",
          "request": {
            "url": "http://example.com/api/?Action=DescribePermissions?IamUserArn=IamUserArn&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the permissions for a specified stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0baefb22-72ab-4ac4-8ff9-268f43c17b67"
            }
          ]
        }
      ]
    },
    {
      "name": "Raid Arrays",
      "item": [
        {
          "id": "a1d63c10-5d58-4a7a-ad2d-47bc7dacc9b2",
          "name": "describeRaidArrays",
          "request": {
            "url": "http://example.com/api/?Action=DescribeRaidArrays?InstanceId=InstanceId&RaidArrayIds=RaidArrayIds&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describe an instance's RAID arrays."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "584432e8-9ea4-4d52-a06a-8e9ccc196155"
            }
          ]
        }
      ]
    },
    {
      "name": "Service Errors",
      "item": [
        {
          "id": "5bbd2174-f183-40ab-aa1c-b41b8ae5c0cb",
          "name": "describeServiceErrors",
          "request": {
            "url": "http://example.com/api/?Action=DescribeServiceErrors?InstanceId=InstanceId&ServiceErrorIds=ServiceErrorIds&StackId=StackId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes AWS OpsWorks Stacks service errors."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "766b82ef-73cb-4f91-9fb2-11fd8a4050f8"
            }
          ]
        }
      ]
    },
    {
      "name": "Host Names",
      "item": [
        {
          "id": "382bdcdb-4191-40da-a3eb-6c30cb59fd76",
          "name": "getHostnameSuggestion",
          "request": {
            "url": "http://example.com/api/?Action=GetHostnameSuggestion?LayerId=LayerId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a generated host name for the specified layer, based on the current host name theme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "722291a3-9f76-4632-8211-6ac0b7ac5096"
            }
          ]
        }
      ]
    }
  ]
}