## 1.0.0 (Released Nov 23, 2022)
- [Remove input properties on Cluster that are not implemented #821](https://github.com/pulumi/pulumi-eks/pull/821)
- [Add support for non-default AWS partitions #788](https://github.com/pulumi/pulumi-eks/pull/788)
- [Add support for launchTemplateTagSpecifications within NodeGroupV2 #810](https://github.com/pulumi/pulumi-eks/pull/810)
- [Use pkg for packaging provider binary #776](https://github.com/pulumi/pulumi-eks/pull/776)
- [Remove default for NodeRootVolumeSize that conflicted with NodeGroupOptions #813](https://github.com/pulumi/pulumi-eks/pull/813)
- [Add support for passing Cluster to NodeGroup/NodeGroupV2/ManagedNodeGroup in all languages #815](https://github.com/pulumi/pulumi-eks/pull/815)
- [Add kubeconfigJson output property to Cluster #815](https://github.com/pulumi/pulumi-eks/pull/815)
- [Adopt plain types in the schema to match the implementation #819](https://github.com/pulumi/pulumi-eks/pull/819)
- [Remove unusable `provider` output from `ClusterCreationRoleProvider` #823](https://github.com/pulumi/pulumi-eks/pull/823)

## 0.42.2 (Released Oct 12, 2022)
- Fix internal registration of NodeGroupV2 resource.
  [#790](https://github.com/pulumi/pulumi-eks/pull/790)

## 0.42.1 (Released Sep 26, 2022)
- Updates to Java SDK.
  [#782](https://github.com/pulumi/pulumi-eks/pull/782)

## 0.42.0 (Released Sep 23, 2022)
- BREAKING CHANGE: Due to https://github.com/pulumi/pulumi/issues/7012 including the provider in the generated SDK never really worked. This is removed now. Note - existing uses in Nodejs should not be affected.
  [#746](https://github.com/pulumi/pulumi-eks/pull/746)
- Fix issue with duplicated AWS_VPC_K8S_CNI_CONFIGURE_RPFILTER env var on aws-node daemonset. 
  [#737](https://github.com/pulumi/pulumi-eks/pull/737)
- Fix an issue where VpcCni options for externalSnat and cniExternalSnat were overwriting each other.
  [#752](https://github.com/pulumi/pulumi-eks/pull/752)
- Add a new version of Node Group, NodeGroupV2. NodeGroupV2 uses Launch Templates in place of Launch Configurations, and Auto Scaling Groups in place of Cloud Formation Stacks. This is expected to become the default in a future release.
- [#766](https://github.com/pulumi/pulumi-eks/pull/766)

## 0.41.2 (Released Jul 12, 2022)
- Allow removal of default Kubernetes addons
  [#732](https://github.com/pulumi/pulumi-eks/pull/732)

## 0.41.1 (Released Jul 10, 2022)
- Export the Cluster IAM Role so that external IAM policies can be attached
  [#730](https://github.com/pulumi/pulumi-eks/pull/730)

## 0.41.0 (Released Jun 21, 2022)
- Add checks to validate versions of kubectl and aws-cli installed
  [#722](https://github.com/pulumi/pulumi-eks/pull/722)

## 0.40.0 (Released May 13, 2022)
- Add enableIpv6 option to clusters
  [#695](https://github.com/pulumi/pulumi-eks/pull/695)
  This change upgrades amazon-vpc-cni-k8s to v1.11.
- Switch kubeconfig to use client.authentication.k8s.io/v1beta1
  [#701](https://github.com/pulumi/pulumi-eks/pull/701)

## 0.39.0 (Released May 9, 2022)
- Add support for Pulumi AWS 5.x
  [#675](https://github.com/pulumi/pulumi-eks/pull/675)

## 0.38.0 (Released May 8, 2022)
- Use apiextensions.k8s.io/v1 for eniconfigs.crd.k8s.amazonaws.com
  [#693](https://github.com/pulumi/pulumi-eks/pull/693)

## 0.37.1 (Released February 10, 2022)
- Ensure Schema is part of the Provider for the GetSchema option
  [#660](https://github.com/pulumi/pulumi-eks/pull/600)

## 0.37.0 (Released February 8, 2022)
- Fix `ENABLE_PREFIX_DELEGATION` not working
  [#646](https://github.com/pulumi/pulumi-eks/pull/646)
- Fix node group's `minSize` and `desiredSize` cannot be 0
  [#645](https://github.com/pulumi/pulumi-eks/issues/645)

## 0.36.0 (Released December 3, 2021)
- Add support for all EC2 LaunchConfiguration EBS parameters related to cluster root node volumes
  [#597](https://github.com/pulumi/pulumi-eks/issues/597)
- Add support for setting `WARM_PREFIX_TARGET` and `ENABLE_PREFIX_DELEGATION`
  [#618](https://github.com/pulumi/pulumi-eks/pull/618)
- NodeGroups accept strings as InstanceTypes
  [#639](https://github.com/pulumi/pulumi-eks/pull/639)

## 0.35.0 (Released November 10, 2021)
- Add support for setting the init container image
  [#631](https://github.com/pulumi/pulumi-eks/pull/631)
- Add support for setting `DISABLE_TCP_EARLY_DEMUX`
  [#631](https://github.com/pulumi/pulumi-eks/pull/631)

## 0.34.0 (Released October 6, 2021)
- Make getKubeconfig method available to multi-lang
  [#628](https://github.com/pulumi/pulumi-eks/pull/628)


## 0.33.0 (Released August 18, 2021)

- Add `capacityType` and `taints` to `ManagedNodeGroup`
  [#614](https://github.com/pulumi/pulumi-eks/pull/614)

## 0.32.0 (Released August 4, 2021)

- Model storageclasses as a map in schema
  [#596](https://github.com/pulumi/pulumi-eks/pull/596)

- Add resource registration for VpcCni (fixes use of NodeGroup)
  [#590](https://github.com/pulumi/pulumi-eks/pull/590)

## 0.31.0 (Released June 8, 2021)

- Upgrade Pulumi dependencies
  [#589](https://github.com/pulumi/pulumi-eks/pull/589)

### Improvements

 - Do not require providerCredentialOpts Cluster parameter when using AWS_PROFILE
   [#561](https://github.com/pulumi/pulumi-eks/pull/561)

## 0.30.0 (Released April 19, 2021)

- Upgrade Pulumi dependencies to 3.0 releases
  [#564](https://github.com/pulumi/pulumi-eks/pull/564)

- Update wording for providerCredentialOpt errors
  [#559](https://github.com/pulumi/pulumi-eks/pull/559)

## 0.23.0 (Released March 22, 2021)

### Improvements

- Go codegen fixes for external references
  [#531](https://github.com/pulumi/pulumi-eks/pull/531)

- Documentation addend for build dependencies
  [#527](https://github.com/pulumi/pulumi-eks/issues/527)

- Expose some more properties to Python, .NET, and Go
  [#536](https://github.com/pulumi/pulumi-eks/pull/536)

- Fix .NET plugin version
  [#542](https://github.com/pulumi/pulumi-eks/pull/542)

- Upgrade version of AWS VPC CNI to v1.7.5
  [#496](https://github.com/pulumi/pulumi-eks/pull/496)

- Upgrade to Go 1.16
  [#548](https://github.com/pulumi/pulumi-eks/pull/548)

- Add support for arm64 plugin binaries
  [#554](https://github.com/pulumi/pulumi-eks/pull/554)

## 0.22.0 (Released January 27, 2021)

### Improvements

- Initial support for Go
  [#519](https://github.com/pulumi/pulumi-eks/pull/519)

- Initial support for Python and .NET
  [#448](https://github.com/pulumi/pulumi-eks/pull/448)

- Add support for `kubernetesServiceIpAddressRange` to `eks.Cluster`
  [#509](https://github.com/pulumi/pulumi-eks/pull/509)

## 0.21.0 (Released January 12, 2021)

### Improvements

- fix(nodejs): Do not fallback on cluster name when creating node group
  This is a breaking change as it will recreate the node group on the first deploy
  [#492](https://github.com/pulumi/pulumi-eks/pull/492)
- fix: correct spelling for encryptRootBlockDevice
  [#450](https://github.com/pulumi/pulumi-eks/pull/450)
- The Node.js SDK now requires an `eks` resource plugin, which will be installed
  automatically during previews/updates (if not already installed).
  [#458](https://github.com/pulumi/pulumi-eks/pull/458)
- Add a flag to allow disabling creation of VPC CNI
  [#493](https://github.com/pulumi/pulumi-eks/pull/493)

## 0.20.0 (Released September 3, 2020)

### Improvements

- Upgrade to `pulumi-aws` v3.0.0
  Note: The move to v3.0.0 of the AWS provider can cause breaking changes if AWS IAM
  InstanceProfiles are used that make use of the plural `.roles` field.
  See [#422](https://github.com/pulumi/pulumi-eks/pull/422) for more details.

### Improvements

## 0.19.5 (Released August 28, 2020)

### Improvements

- feat(nodegroup): add nodeUserDataOverride arg to specify userdata script
  [#429](https://github.com/pulumi/pulumi-eks/pull/429)
- fix(fargate): ensure fargate profile name is valid
  [#430](https://github.com/pulumi/pulumi-eks/pull/430)
- fix(cluster): add https req timeout & show time left waiting for healthz
  [#427](https://github.com/pulumi/pulumi-eks/pull/427)
- fix(kubeconfig): treat auth & env as Output<t> in kubeconfig generation
  [#421](https://github.com/pulumi/pulumi-eks/pull/421)
- examples: Add VPC & subnet tag example for subnets managed with Pulumi
  [#420](https://github.com/pulumi/pulumi-eks/pull/420)

## 0.19.4 (Released August 11, 2020)

- Support for the ENI_CONFIG_LABEL_DEF environment variable
  [#411](https://github.com/pulumi/pulumi-eks/pull/411)

### Improvements

## 0.19.3 (Released July 7, 2020)

### Improvements

- feat(nodegroup): Support encryption of the root block device for nodes
  [#407](https://github.com/pulumi/pulumi-eks/pull/407)
- fix(ex/default-sg): rm Output tag values per string type reqs
  [#404](https://github.com/pulumi/pulumi-eks/pull/404)
- nodegroup(asgName): fix asgName definition
  [#401](https://github.com/pulumi/pulumi-eks/pull/401)

## 0.19.2 (Released May 20, 2020)

### Improvements

- Cutting new release to include missing generated API docs from v0.19.1

## 0.19.1 (Released May 19, 2020)

### Improvements

- feat(nodegroup): add opt to attach extra security groups
  [#390](https://github.com/pulumi/pulumi-eks/pull/390)
- feat(cluster): add encryptionConfigKeyArn opt to encrypt k8s Secrets
  [#389](https://github.com/pulumi/pulumi-eks/pull/389)

## 0.19.0 (Released April 20, 2020)

**For a more detailed list of the changes introduced in this release, please
visit [#381](https://github.com/pulumi/pulumi-eks/pull/381).**

- fix(dashboard): disable dashboard from deploying if not set
  [#378](https://github.com/pulumi/pulumi-eks/pull/378)
- fix(cluster): use scoped kubeconfig with non-default AWS credentials
  [#367](https://github.com/pulumi/pulumi-eks/pull/367)
- Update node & go pulumi deps to 2.0
  [#375](https://github.com/pulumi/pulumi-eks/pull/375)
- fix(aws): rm sync invokes for AWS data source calls
  [#373](https://github.com/pulumi/pulumi-eks/pull/373)
- refactor(aws-auth): replace aws-iam-authenticator with aws eks get-token
  [#362](https://github.com/pulumi/pulumi-eks/pull/362)
    - **Note:** for existing clusters, this change will recompute the kubeconfig
    used, as its auth arguments and settings get updated to work with
    `aws eks get-token`. It should not affect cluster access or cause
    replacements of existing k8s resources.
- feat(nodegroup): use the latest recommended AMIs from the SSM store
  [#366](https://github.com/pulumi/pulumi-eks/pull/366)
- feat(cluster): support HTTP(S) proxy for cluster readiness & OIDC config
  [#365](https://github.com/pulumi/pulumi-eks/pull/365)
- deps(pulumi): bump node and go pulumi/pulumi to v1.13.1
  [#361](https://github.com/pulumi/pulumi-eks/pull/361)
- feat(cluster): add getKubeconfig method to generate scoped kubeconfigs
  [#356](https://github.com/pulumi/pulumi-eks/pull/356)

## 0.18.24 (Released March 11, 2020)

### Improvements

- fix(oidc): Fix issue in OIDC getThumbprint helper function
  [#346](https://github.com/pulumi/pulumi-eks/pull/346)

## 0.18.23 (Released March 5, 2020)

### Improvements

- fix(oidc): use thumbprint of the intermediate root CA
  [#342](https://github.com/pulumi/pulumi-eks/pull/342)

## 0.18.22 (Released February 24, 2020)

### Improvements

- update(cni): update from v1.5.3 -> v1.6.0
  [#325](https://github.com/pulumi/pulumi-eks/pull/325)
- fix(storageClasses): fix userStorageClass initialization
  [#336](https://github.com/pulumi/pulumi-eks/pull/336)
- feat(cluster): allow optional configuration of cluster name
  [#322](https://github.com/pulumi/pulumi-eks/pull/322)
- feat(identity): add support to setup OIDC provider
  [#320](https://github.com/pulumi/pulumi-eks/pull/320)

## 0.18.21 (Released February 12, 2020)

### Improvements

- Refactor managed nodegroup API and require its role be provided to the cluster
  [#302](https://github.com/pulumi/pulumi-eks/pull/302)
- Update pulumi/pulumi and re-enable withUpdate tests
  [#327](https://github.com/pulumi/pulumi-eks/pull/327)

## 0.18.20 (Released February 11, 2020)

### Improvements

- Fix js-yaml dependency changes in pulumi/k8s
  [#324](https://github.com/pulumi/pulumi-eks/pull/324)

## 0.18.19 (Released January 27, 2020)

### Improvements

- Unblock CI by disabling debug logging, rm unnecessary tests, and fixing broken tests
  [#309](https://github.com/pulumi/pulumi-eks/pull/309)
- feat(cluster): Support public access controls
  [#295](https://github.com/pulumi/pulumi-eks/issues/295)
- feat(cluster): Add cluster tagging
  [#262](https://github.com/pulumi/pulumi-eks/pull/262)
- refactor(vpcCni): set node anti-affinity to not deploy to fargate
  [#291](https://github.com/pulumi/pulumi-eks/pull/291)
- build: Upgrade to go1.13.4
  [#290](https://github.com/pulumi/pulumi-eks/pull/290)

## 0.18.18 (Released December 5, 2019)

### Improvements

- feat(nodes): add support for Fargate
  [#283](https://github.com/pulumi/pulumi-eks/pull/283)

## 0.18.17 (Released December 3, 2019)

### Improvements

- feat(nodes): add createManagedNodeGroup
  [#280](https://github.com/pulumi/pulumi-eks/pull/280)

## 0.18.16 (Released November 7, 2019)

### Improvements

- fix(vpc-cni): allow logLevel & logFile to be set, or defaulted if not
  [#274](https://github.com/pulumi/pulumi-eks/pull/274)
- Update pulumi to 1.4.0
  [#270](https://github.com/pulumi/pulumi-eks/pull/270)

## 0.18.15 (Released October 15, 2019)

### Improvements

- refactor(cluster): allow ClusterOptions to accept NodeGroupOptions
  [#259](https://github.com/pulumi/pulumi-eks/pull/259)

## 0.18.14 (Released September 5, 2019)

### Improvements

- Add new publicSubnetIds and privateSubnetIds cluster options. Also, update
  tests to use new awsx.ec2.Vpc API and new subnet options
  [#238](https://github.com/pulumi/pulumi-eks/pull/238)
- fix(iam): improve YAML error handling & reporting in IAM ops
  [#231](https://github.com/pulumi/pulumi-eks/pull/231)

## 0.18.13 (Released August 20, 2019)

### Improvements

- feat(iam): create eks cluster & resources with iam role provider
  [#205](https://github.com/pulumi/pulumi-eks/pull/205)

## 0.18.12 (Released August 16, 2019)

### Improvements

- fix(cni): read CNI YAML outside of the dynamic provider and update to v1.5.3
  [#223](https://github.com/pulumi/pulumi-eks/pull/223)

## 0.18.11 (Released August 12, 2019)

### Improvements

- Revert "fix(cni): modify CNI filepath to store the relative path"
  [#220](https://github.com/pulumi/pulumi-eks/pull/220)

## 0.18.10 (Released August 8, 2019)

### Improvements

- Fix and improve migrate-nodegroup test (bump CNI from `v1.5.0` -> `v1.5.2`)
  [#214](https://github.com/pulumi/pulumi-eks/pull/214)
- fix(asgName): check 'NodeGroup' CFStack output key exists
  [#213](https://github.com/pulumi/pulumi-eks/pull/213)
- chore(cluster): add deprecation for kube-dashboard, customInstanceRolePolicy
  [#202](https://github.com/pulumi/pulumi-eks/pull/202)
- feat(storage-classes): export all user created storage classes
  [#172](https://github.com/pulumi/pulumi-eks/pull/172)
- update(eks): add example of migrating node groups with zero downtime
  [#195](https://github.com/pulumi/pulumi-eks/pull/195)

## 0.18.9 (Released July 11, 2019)

### Improvements

- refactor(secgroup): export createNodeGroupSecurityGroup & consolidate rules
  [#183](https://github.com/pulumi/pulumi-eks/pull/183)
- wait for EKS cluster endpoint to be available
  [#193](https://github.com/pulumi/pulumi-eks/pull/193)
- fix(cluster): support configuring private and public endpoint access
  [#154](https://github.com/pulumi/pulumi-eks/pull/154)
- fix(cluster): support passing additional arguments to /etc/eks/bootstrap.sh and --kubelet-extra-args
  [#181](https://github.com/pulumi/pulumi-eks/pull/181)

## 0.18.8 (Released June 19, 2019)

### Improvements

- Default to a node AMI that matches the cluster version
  [#175](https://github.com/pulumi/pulumi-eks/pull/175)
- fix(tags): rm ASG tag dupes, and consider tag inheritance for all tags
  [#162](https://github.com/pulumi/pulumi-eks/pull/162)
- fix(nodegroup): make VPN-only subnets private
  [#163](https://github.com/pulumi/pulumi-eks/pull/163)

- feature(cluster): Allow service role and instance profile to be injected during cluster creation
  [#159](https://github.com/pulumi/pulumi-eks/pull/159)

## 0.18.7 (Released June 12, 2019)

### Improvements

- ci(aws-iam-authenticator): use official S3 bucket to install bin
  [#166](https://github.com/pulumi/pulumi-eks/pull/166)
- fix(tags): change map types used in all tags to pulumi.Inputs of the map
  [#157](https://github.com/pulumi/pulumi-eks/pull/157)
- fix(cluster): expose instanceRoles
  [#155](https://github.com/pulumi/pulumi-eks/pull/155)
- tests(cluster): enable test to replace cluster by adding more subnets
  [#150](https://github.com/pulumi/pulumi-eks/pull/150)
- update(aws-k8s-cni): move from 1.4.1 -> 1.5.0
  [#148](https://github.com/pulumi/pulumi-eks/pull/148)

## 0.18.6 (Released June 04, 2019)

### Improvements

- fix(cluster): rm dupe default storage class
  [#136](https://github.com/pulumi/pulumi-eks/pull/136)
- Expand nodejs SDK tests coverage, and add Kubernetes Smoke Tests for examples
  & tests [#130](https://github.com/pulumi/pulumi-eks/pull/130)
- update(aws-k8s-cni): move from 1.3.0 -> 1.4.1
  [#134](https://github.com/pulumi/pulumi-eks/pull/134)
- fix(cluster): export missing instanceRoles in the cluster's CoreData
  [#133](https://github.com/pulumi/pulumi-eks/pull/133)

## 0.18.5 (Released May 09, 2019)

### Improvements

- fix(nodeSecurityGroupTags): only expose option through Cluster class
  [#126](https://github.com/pulumi/pulumi-eks/pull/126)
- fix(secgroups): do not null out ingress & egress
  [#128](https://github.com/pulumi/pulumi-eks/pull/128)
    - Note: This PR reverses the default null values used for the
      ingress and egress in-line rules of the secgroups, introduced in `v0.18.3`.
      The null default was required to move to standalone secgroup rules, but it
      has introduced [issues](https://github.com/pulumi/pulumi-eks/issues/127), and thus is being removed in this PR.
    - Upgrade Path - This is a breaking change **unless** you do the following steps:
      - If using >= `v0.18.3`: update using the typical package update path.
      - If using <= `v0.18.2`:
        1. First, update your cluster from using your current version to `v0.18.4`.
        1. Next, update your cluster from `v0.18.4` to `v0.18.5` (or higher) using the typical package update path.

## 0.18.4 (Released May 02, 2019)

### Improvements

- feat(tags): Set default tags & add opts: tags, and other resource tags
  [#122](https://github.com/pulumi/pulumi-eks/pull/122)
- feat(control plane logging): Enable control plane logging to cloudwatch.
  [#100](https://github.com/pulumi/pulumi-eks/pull/117).
- fix(ami): only apply AMI smart-default selection on creation
  [#114](https://github.com/pulumi/pulumi-eks/pull/114)

## 0.18.3 (Released April 25, 2019)

### Improvements

- fix(secgroups): use standalone secgroup rules instead of in-line rules
  [#109](https://github.com/pulumi/pulumi-eks/pull/109). Note, because we are
  replacing existing in-line secgroup rules with standalone rules,
  there may be a brief period of outage where the security group rules are
  removed before they get added back. This update happens in a matter of
  seconds (~5 sec), so any interruptions are short-lived.

## 0.18.2 (Released April 24, 2019)

### Improvements

- fix(nodegroup): filter on x86_64 arch for node AMI
  [#112](https://github.com/pulumi/pulumi-eks/pull/112)

## 0.18.1 (Released April 08, 2019)

### Improvements

- feat(nodePools): support per-nodegroup IAM instance roles
  [#98](https://github.com/pulumi/pulumi-eks/pull/98)

## 0.18.0 (Released March 30, 2019)

### Improvements

- Moves to the new 0.18.0 version of `@pulumi/aws`.  Version 0.18.0 of `pulumi-aws` is now based on
  v2.2.0 of the AWS Terraform Provider, which has a variety of breaking changes from the previous
  version. See documentation in `@pulumi/aws` repo for more details.

## 0.17.4 (Released March 29, 2019)

### Improvements

- Fix a bug where the regex used to retrieve Worker Node AMIs was not
  returning correct AMIs when either: specifying the master / control plane
  version, or relying on smart defaults of the lastest available image. [#92](https://github.com/pulumi/pulumi-eks/pull/92)

## 0.17.3 (Released March 28, 2019)

### Improvements

- feat(workers): add 'nodeAssociatePublicIpAddress' to toggle public IPs
  [#81](https://github.com/pulumi/pulumi-eks/pull/81)
- fix(getAmi): allow setting master version & explicitly filter Linux AMIs
  [#85](https://github.com/pulumi/pulumi-eks/pull/85)
  - Fix a bug where the wrong AMI was being returned due to a loosely defined
    regex.
  - Add support for setting the master / control plane version of the cluster.

## 0.17.2 (Released March 19, 2019)

### Improvements

- Re-cut 0.17.1 as 0.17.2, due to a broken master branch caused by a pushed tag
publishing the NPM package before master was able to.

## 0.17.1 (Released March 19, 2019)

### Improvements

- Support for `taints` on `NodeGroups`. [#63](https://github.com/pulumi/pulumi-eks/pull/63)

## 0.17.0 (Released March 6th, 2019)

### Improvements

- Depend on latest version of `@pulumi/pulumi` to get more precise delete before create semantics [#46](https://github.com/pulumi/pulumi-eks/issues/46)

## 0.16.6 (Released January 29th, 2019)

### Improvements

- Expose the AutoScalingGroup on NodeGroups. [#53](https://github.com/pulumi/pulumi-eks/pull/53)
- Fix a bug where `desiredCapacity` was not being handled correctly. [#55](https://github.com/pulumi/pulumi-eks/pull/55)

## 0.16.5 (Released January 21st, 2019)

### Improvements

- Support for multiple Worker `NodeGroup`s connected to a single EKS cluster. [#39](https://github.com/pulumi/pulumi-eks/issues/39)
- Support for Spot instances in `NodeGroup`s. [#49](https://github.com/pulumi/pulumi-eks/pull/49)
- Support for adding cutom policies to node `InstanceRole`. [#49](https://github.com/pulumi/pulumi-eks/pull/49)
- Support for adding labels to each instance in a `NodeGroup`. [#49](https://github.com/pulumi/pulumi-eks/pull/49)

## 0.16.4 (Released December 13th, 2018)

### Improvements

- Expose underlying EKS `cluster`. [#31](https://github.com/pulumi/pulumi-eks/pull/31)
- Support custom worker node AMI. [#34](https://github.com/pulumi/pulumi-eks/pull/34)
- Update CNI to 1.3. [#37](https://github.com/pulumi/pulumi-eks/pull/37)

## 0.16.3 (Released November 21st, 2018)

### Improvements

- Allow configuring the subnets that worker nodes use.
- Improve detection of public vs. private subnets.
