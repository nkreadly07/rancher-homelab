----- Starting hook: ./bootstrap.sh
### Bootstrap
### Warning: running container as root user
----- Starting hook: /opt/entrypoint.sh
Command: start-server
Processing secrets in SECRETS_DIR (if any)...
################################################################################
#    Ping Identity DevOps Docker Image
#     IMAGE_VERSION: pingdirectory-alpine_3.13-az11-8.3.0.0-210707-3a30
#     IMAGE_GIT_REV: 3a306df97838ae0c156a0b78851464c369ab8d74
#           STARTED: Tue Sep 13 15:52:26 UTC 2022
#          HOST_NAME: pingdirectory-0
#        DOMAIN_NAME: 
################################################################################
rm: can't remove '/opt/staging/topology/descriptor.json': Resource busy
rmdir: '/opt/staging/topology': Directory not empty
rm: can't remove '/opt/staging/topology.json': Resource busy
rm: can't remove '/opt/staging/jmx_prometheus_javaagent-0.14.0.jar': Resource busy
rm: can't remove '/opt/staging/ds_env_vars': Resource busy
rm: can't remove '/opt/staging/newrelic.jar': Resource busy
copying local IN_DIR files (/opt/in) to STAGING_DIR (/opt/staging)

----- Starting hook: /opt/staging/hooks/01-start-server.sh

----- Starting hook: /opt/staging/hooks/02-get-remote-server-profile.sh
Getting SERVER_PROFILE
  git url: *** REDACTED ***
   branch: dev
     path: profiles/pingdirectory
Checking for security filename issues...*.jwk *.pin
   PASSED

No previous state to compare.


----- Starting hook: /opt/staging/hooks/03-build-run-plan.sh
We are the SEED server (pingdirectory-0.pingdirectory)

    ###################################################################################
    #
    #                      PD_STATE: UPDATE
    #                      RUN_PLAN: RESTART
    #

    ###################################################################################
    #            ORCHESTRATION_TYPE: KUBERNETES
    #                      HOST_NAME: pingdirectory-0
    #                    serverUUID: 814f0fbe-5560-30ab-8fa3-68a985de38ca
    #
#
    #         K8S_STATEFUL_SET_NAME: pingdirectory
    # K8S_STATEFUL_SET_SERVICE_NAME: pingdirectory
    #
    #                  K8S_CLUSTERS:   (single cluster)
    #                   K8S_CLUSTER: 
    #              K8S_SEED_CLUSTER: 
    #              K8S_NUM_REPLICAS: 
    #       K8S_POD_HOSTNAME_PREFIX: 
    #       K8S_POD_HOSTNAME_SUFFIX: 
    #      K8S_SEED_HOSTNAME_SUFFIX: 
    #           K8S_INCREMENT_PORTS:  ()
    #
    #
    #     Startup Plan
    #        - manage-profile replace-profile
    #        - repl enable (from SEED Server-pingdirectory-0.pingdirectory)
    #        - repl init   (from topology.json, from SEED Server-pingdirectory-0.pingdirectory)
    ###################################################################################
    #
    # POD Server Information
    #                 instance name: pingdirectory-0.pingdirectory
    #                      hostname: pingdirectory-0.pingdirectory
    #                      location: Austin
    #                    ldaps port: 1636
    #              replication port: 8989
    #
    # SEED Server Information
    #                 instance name: pingdirectory-0.pingdirectory
    #                      hostname: pingdirectory-0.pingdirectory
    #                      location: Austin
    #                    ldaps port: 1636
    #              replication port: 8989
    ###################################################################################
    


----- Starting hook: /opt/staging/hooks/04-check-variables.sh
################################################################################
################################################################################
###################### WARNING - DEPRECATED VARIABLES ##########################
#  The following deprecated variables were found. These variables may be removed
#  in a future release.

                            DOLLAR : $ 

################################################################################

################################################################################
#    Docker Image Information
################################################################################
                     IMAGE_VERSION : pingdirectory-alpine_3.13-az11-8.3.0.0-210707-3a30 
                     IMAGE_GIT_REV : 3a306df97838ae0c156a0b78851464c369ab8d74 
                         HOST_NAME : pingdirectory-0 
                       DOMAIN_NAME : --- empty --- 
################################################################################
#    Directory Variables
################################################################################
                              BASE : /opt 
                            IN_DIR : /opt/in 
                           OUT_DIR : /opt/out 
                   SERVER_ROOT_DIR : /opt/out/instance 
                       STAGING_DIR : /opt/staging 
                         HOOKS_DIR : /opt/staging/hooks 
                SERVER_PROFILE_DIR : /tmp/server-profile 
                           BAK_DIR : /opt/backup 
                          LOGS_DIR : /opt/logs 
                       SECRETS_DIR : /usr/local/secrets 
                       LICENSE_DIR : /opt/out/instance 
################################################################################
#    File Variables
################################################################################
                     TOPOLOGY_FILE : /opt/staging/topology.json 
                    TAIL_LOG_FILES : --- empty --- 
                     COLORIZE_LOGS : true 
################################################################################
#    Server Profile
################################################################################
                SERVER_PROFILE_URL : *** REDACTED *** 
             SERVER_PROFILE_BRANCH : dev 
               SERVER_PROFILE_PATH : profiles/pingdirectory 
             SERVER_PROFILE_UPDATE : true 
################################################################################
#    Security Checks
################################################################################
            SECRUITY_CHECKS_STRICT : --- empty --- 
          SECURITY_CHECKS_FILENAME : *.jwk *.pin 
################################################################################
#    DevOps User/Key
################################################################################
         PING_IDENTITY_DEVOPS_USER : ssm://pcpt/devops-license/user 
          PING_IDENTITY_DEVOPS_KEY : *** REDACTED *** 
################################################################################
#    License Key Info
################################################################################
                 LICENSE_FILE_NAME : PingDirectory.lic 
                LICENSE_SHORT_NAME : PD 
                   LICENSE_VERSION : 8.3 
         MUTE_LICENSE_VERIFICATION : --- empty --- 
################################################################################
#    Product Startup
################################################################################
                   STARTUP_COMMAND : /opt/out/instance/bin/start-server 
           STARTUP_FOREGROUND_OPTS : --nodetach 
           STARTUP_BACKGROUND_OPTS : --- empty --- 
                           VERBOSE : false 
                        PING_DEBUG : false 
                 CLEAN_STAGING_DIR : true 
################################################################################
#    Orchestration Info
################################################################################
                ORCHESTRATION_TYPE : KUBERNETES 
                      K8S_CLUSTERS : --- empty --- 
                       K8S_CLUSTER : --- empty --- 
                  K8S_SEED_CLUSTER : --- empty --- 
                  K8S_NUM_REPLICAS : --- empty --- 
           K8S_POD_HOSTNAME_PREFIX : --- empty --- 
           K8S_POD_HOSTNAME_SUFFIX : --- empty --- 
          K8S_SEED_HOSTNAME_SUFFIX : --- empty --- 
               K8S_INCREMENT_PORTS : --- empty --- 
################################################################################
#    Ping Product Info
################################################################################
                      PING_PRODUCT : PingDirectory 
                          LOCATION : Austin 
                         LDAP_PORT : 1389 
                        LDAPS_PORT : 1636 
                        HTTPS_PORT : 1443 
                          JMX_PORT : 1689 
                      USER_BASE_DN : dc=amstock,dc=com 
         PD_ENGINE_PUBLIC_HOSTNAME : localhost 
          PF_ADMIN_PUBLIC_HOSTNAME : pingfederate-admin.dev-astfinancial.us1.ping.cloud 
         PF_ENGINE_PUBLIC_HOSTNAME : pingfederate.dev-astfinancial.us1.ping.cloud 
          PA_ADMIN_PUBLIC_HOSTNAME : pingaccess-admin.dev-astfinancial.us1.ping.cloud 
         PA_ENGINE_PUBLIC_HOSTNAME : pingaccess.dev-astfinancial.us1.ping.cloud 
           PF_ADMIN_PUBLIC_BASEURL : https://localhost:9999 
                      ROOT_USER_DN : cn=administrator 
             ADDITIONAL_SETUP_ARGS : --- empty --- 
################################################################################
#    JVM Details
################################################################################
                     MAX_HEAP_SIZE : 3g 
                        JVM_TUNING : AGGRESSIVE 
################################################################################



----- Starting hook: /opt/staging/hooks/05-expand-templates.sh
expanding files...
  Processing templates
    t - ./pd.profile/dsconfig/13-global-aci-grants.dsconfig.subst
  Processing defaults
    d - ./instance/config/java.properties.aarch64.subst.default .. skipped
    d - ./pd.profile/dsconfig/01-license-gauge.dsconfig.subst.default .. expanded
    d - ./pd.profile/dsconfig/01-remove-console.dsconfig.subst.default .. skipped
    d - ./pd.profile/dsconfig/01-remove-host-monitor.dsconfig.subst.default .. expanded


----- Starting hook: /opt/staging/hooks/06-copy-product-bits.sh


----- Starting hook: /opt/staging/hooks/07-apply-server-profile.sh
merging /opt/staging/instance to /opt/out/instance


----- Starting hook: /opt/staging/hooks/09-build-motd.sh
Successfully downloaded MOTD from https://raw.githubusercontent.com/pingidentity/pingidentity-devops-getting-started/master/motd/motd.json
Current /etc/motd
    
    ################################################################################
                    Ping Identity DevOps Docker Image
    
           Version: pingdirectory-alpine_3.13-az11-8.3.0.0-210707-3a30
       DevOps User: ssm://pcpt/devops-license/user
          Hostname: pingdirectory-0
           Started: Tue Sep 13 15:52:31 UTC 2022
    ################################################################################
    
    Server Profile pingdirectory
      - Creates an initial PingDirectory with users
      - Prepared for connections from DataSync, DirectoryProxy and DataGovernance
    
    
    ################################################################################


----- Starting hook: /opt/staging/hooks/20-restart-sequence.sh.pre

----- Starting hook: /opt/staging/hooks/10-download-artifact.sh
10-download-artifact.sh: 2022-09-13 15:52:31 INFO export config settings
10-download-artifact.sh: 2022-09-13 15:52:31 INFO MULTI_CLUSTER - false
10-download-artifact.sh: 2022-09-13 15:52:31 INFO PRIMARY_CLUSTER - true
10-download-artifact.sh: 2022-09-13 15:52:31 INFO PD_HTTPS_PORT - 1443
10-download-artifact.sh: 2022-09-13 15:52:31 INFO PD_LDAP_PORT - 1389
10-download-artifact.sh: 2022-09-13 15:52:31 INFO PD_LDAPS_PORT - 1636
10-download-artifact.sh: 2022-09-13 15:52:31 INFO PD_REPL_PORT - 8989
10-download-artifact.sh: 2022-09-13 15:52:31 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
10-download-artifact.sh: 2022-09-13 15:52:31 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
10-download-artifact.sh: 2022-09-13 15:52:31 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
10-download-artifact.sh: 2022-09-13 15:52:31 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
10-download-artifact.sh: 2022-09-13 15:52:31 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
10-download-artifact.sh: 2022-09-13 15:52:31 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
10-download-artifact.sh: 2022-09-13 15:52:31 INFO Private Repo : s3://bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7
10-download-artifact.sh: 2022-09-13 15:52:31 INFO Public Repo  : https://ping-artifacts.s3-us-west-2.amazonaws.com
10-download-artifact.sh: 2022-09-13 15:52:31 INFO [
  {
    "name": "pingdata-extensions",
    "version": "1.0.2",
    "filename": "pingdata-extensions-1.0.2.zip"
  },
  {
    "name": "session-revocation",
    "version": "1.0.1",
    "filename": "pd-session-revocation-1.0.1.zip",
    "source": "private"
  }
]
10-download-artifact.sh: 2022-09-13 15:52:32 INFO Download Artifact from https://ping-artifacts.s3-us-west-2.amazonaws.com/pingdirectory/pingdata-extensions/1.0.2
10-download-artifact.sh: 2022-09-13 15:52:32 INFO Artifact successfully downloaded.
10-download-artifact.sh: 2022-09-13 15:52:32 INFO Validating downloaded artifact file
10-download-artifact.sh: 2022-09-13 15:52:32 INFO Download Artifact from s3://bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7/pingdirectory/session-revocation/1.0.1
10-download-artifact.sh: 2022-09-13 15:52:32 INFO Copying: 'pd-session-revocation-1.0.1.zip' to '/opt/staging/pd.profile/server-sdk-extensions'
2022/09/13 15:52:32 Downloading file: s3://bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7/pingdirectory/session-revocation/1.0.1/pd-session-revocation-1.0.1.zip 
2022/09/13 15:52:32 Bucket: bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7 File: pingdirectory/session-revocation/1.0.1/pd-session-revocation-1.0.1.zip
2022/09/13 15:52:32 Using AWS_REGION: us-east-2
2022/09/13 15:52:32 Concurrency: 0 PartSize: 0
2022/09/13 15:52:32 File: pd-session-revocation-1.0.1.zip  Size: 9331451 bytes
2022/09/13 15:52:32 Successfully downloaded file: /opt/staging/pd.profile/server-sdk-extensions/pd-session-revocation-1.0.1.zip
10-download-artifact.sh: 2022-09-13 15:52:32 INFO Validating downloaded artifact file
pd-session-revocation-1.0.1.zip pingdata-extensions-1.0.2.zip

----- Starting hook: /opt/staging/hooks/20-restart-sequence.sh
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO export config settings
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO MULTI_CLUSTER - false
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO PRIMARY_CLUSTER - true
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO PD_HTTPS_PORT - 1443
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO PD_LDAP_PORT - 1389
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO PD_LDAPS_PORT - 1636
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO PD_REPL_PORT - 8989
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO restarting container
20-restart-sequence.sh: 2022-09-13 15:52:32 INFO Re-generating java.properties for current JVM

The operation was successful.  The Directory Server commands will use the java
arguments and java home specified in the properties file located in
/opt/out/instance/config/java.properties
20-restart-sequence.sh: 2022-09-13 15:52:47 INFO restart-sequence: updating server profile



20-restart-sequence.sh: 2022-09-13 15:52:47 INFO Copying the license key into the PD profiles directory
20-restart-sequence.sh: 2022-09-13 15:52:47 INFO Using /usr/local/secrets/encryption-settings.pin as the encryption-setting.pin file
20-restart-sequence.sh: 2022-09-13 15:52:47 INFO Merging changes from new server profile
Validating source and existing servers ..... Done
Exporting the encryption settings definitions to temporary file
/tmp/encryption-settings-export-4009881715004361126.tmp

Preparing existing server ..... Done
Setting up the server with the new profile ..... Done
Importing the encryption settings definitions from temporary file
/tmp/encryption-settings-export-4009881715004361126.tmp
Skipping export and re-import since the "--reimportData never" argument was
specified

Merging in configuration and data from the existing server ..... Done
Merging in topology and license configuration from the existing server ..... Done
Setting the inter-server certificate ..... Done
Validating server ..... Done
Cleaning up after replace ..... Done
20-restart-sequence.sh: 2022-09-13 15:55:12 INFO manage-profile replace-profile status: 0
20-restart-sequence.sh: 2022-09-13 15:55:12 INFO Copy beluga profile files after restart

----- Starting hook: /opt/staging/hooks/07-apply-server-profile.sh
merging /opt/staging/instance to /opt/out/instance

20-restart-sequence.sh: 2022-09-13 15:55:21 INFO Not rebuilding indexes as there are no indexes to rebuild with status NEW or UNTRUSTED
20-restart-sequence.sh: 2022-09-13 15:55:21 INFO updating tools.properties

----- Starting hook: /opt/staging/hooks/185-apply-tools-properties.sh
Configuring tools.properties

20-restart-sequence.sh: 2022-09-13 15:55:21 INFO updating encryption settings

----- Starting hook: /opt/staging/hooks/15-encryption-settings.sh
15-encryption-settings.sh: 2022-09-13 15:55:21 INFO export config settings
15-encryption-settings.sh: 2022-09-13 15:55:21 INFO MULTI_CLUSTER - false
15-encryption-settings.sh: 2022-09-13 15:55:21 INFO PRIMARY_CLUSTER - true
15-encryption-settings.sh: 2022-09-13 15:55:21 INFO PD_HTTPS_PORT - 1443
15-encryption-settings.sh: 2022-09-13 15:55:21 INFO PD_LDAP_PORT - 1389
15-encryption-settings.sh: 2022-09-13 15:55:21 INFO PD_LDAPS_PORT - 1636
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO PD_REPL_PORT - 8989
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO encryption-settings: starting processing of encryption-settings definitions
15-encryption-settings.sh: 2022-09-13 15:55:22 INFO encryption-settings: creating a new encryption definition
15-encryption-settings.sh: 2022-09-13 15:55:27 INFO encryption-settings: Unable to add the new encryption settings definition for use in the server:
Encryption settings definition
E6FCD9B397C6B66C6BCC55E623FB50C1B46C15C145A7CD08C9E53D0E60249274 already
exists in the database (id=1879310781 EncryptionSettingsDB.java:999
8.3.0.0-20210617212340.000Z-29a2bc05).
15-encryption-settings.sh: 2022-09-13 15:55:27 INFO encryption-settings: finished processing all encryption-settings definitions

20-restart-sequence.sh: 2022-09-13 15:55:27 INFO enabling the replication sub-system in offline mode
20-restart-sequence.sh: 2022-09-13 15:55:27 INFO configuring userRoot for base DN dc=amstock,dc=com

Arguments from tool properties file:  --useSSL  --hostname localhost --port
1636 --bindDN cn=administrator --bindPasswordFile
/usr/local/secrets/root-user-password --trustAll


One or more configuration property changes require administrative action or
confirmation/notification.  Those properties include:

 * base-dn:  No administrative action is required by default although some
 action may be required on a per-backend basis before the new base DN may be
 used.
Although it is currently supported, the use of multiple base DNs per backend
is not recommended and this capability may be removed in the future. If you
are considering the use of multiple base DNs in a backend, you should first
contact Ping Identity support to discuss this configuration.


The Local DB Backend was modified successfully
20-restart-sequence.sh: 2022-09-13 15:55:40 INFO configure base DN dc=amstock,dc=com update status: 0
20-restart-sequence.sh: 2022-09-13 15:55:49 INFO Number of sub entries of DN dc=amstock,dc=com in userRoot backend: 44518
20-restart-sequence.sh: 2022-09-13 15:55:49 INFO Replication base DN dc=amstock,dc=com already added
20-restart-sequence.sh: 2022-09-13 15:55:49 INFO add base DN dc=amstock,dc=com status: 0
----- Starting hook: /opt/staging/hooks/185-offline-enable-wrapper.sh
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO export config settings
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO MULTI_CLUSTER - false
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO PRIMARY_CLUSTER - true
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO PD_HTTPS_PORT - 1443
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO PD_LDAP_PORT - 1389
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO PD_LDAPS_PORT - 1636
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO PD_REPL_PORT - 8989
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable-wrapper.sh: 2022-09-13 15:55:49 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable-wrapper.sh: 2022-09-13 15:55:50 INFO Topology descriptor file does not exist or is empty - creating it at /tmp/tmp.annjlP
185-offline-enable-wrapper.sh: 2022-09-13 15:55:50 INFO Topology descriptor JSON file '/tmp/tmp.annjlP' contents:
{"us-east-2":{"hostname":"pingdirectory.ping-cloud.svc.cluster.local","replicas":3}}
185-offline-enable-wrapper.sh: 2022-09-13 15:55:50 INFO offline enable configuration:
{
  "descriptor_json"     : "/tmp/tmp.annjlP",
  "inst_root"           : "/opt/out/instance",
  "hostname_prefix"     : "pingdirectory",
  "local_tenant_domain" : "astfinancial.us1.ping.cloud",
  "local_region"        : "us-east-2",
  "local_num_replicas"  : 3,
  "local_ordinal"       : 0,
  "repl_id_base"        : 1000,
  "repl_id_rinc"        : 1000,
  "repl_id_inc"         : 100,
  "https_port_base"     : 1443,
  "ldap_port_base"      : 1389,
  "ldaps_port_base"     : 1636,
  "repl_port_base"      : 8989,
  "port_inc"            : 0,
  "ads_crt_file"        : "/usr/local/secrets/ads.crt",
  "admin_user"          : "admin",
  "admin_pass_file"     : "/usr/local/secrets/admin-user-password"
}
----- Starting hook: /opt/staging/hooks/185-offline-enable.sh
185-offline-enable.sh: 2022-09-13 15:55:50 INFO export config settings
185-offline-enable.sh: 2022-09-13 15:55:50 INFO MULTI_CLUSTER - false
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PRIMARY_CLUSTER - true
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_HTTPS_PORT - 1443
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_LDAP_PORT - 1389
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_LDAPS_PORT - 1636
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_REPL_PORT - 8989
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:55:50 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:55:50 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
185-offline-enable.sh: 2022-09-13 15:55:50 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:55:50 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:55:50 INFO export config settings
185-offline-enable.sh: 2022-09-13 15:55:50 INFO MULTI_CLUSTER - false
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PRIMARY_CLUSTER - true
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_HTTPS_PORT - 1443
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_LDAP_PORT - 1389
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_LDAPS_PORT - 1636
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_REPL_PORT - 8989
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:55:50 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:55:50 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:55:50 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
185-offline-enable.sh: 2022-09-13 15:55:50 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:55:50 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:55:50 INFO Begin for '/opt/out/instance'
Processing completed.  Transformed 707 entries.
185-offline-enable.sh: 2022-09-13 15:55:54 INFO Difference between /opt/out/instance/config/config.ldif and /tmp/185-offline-enable.sh.XXXXKfCKND/config.ldif.nowrap
--- /opt/out/instance/config/config.ldif
+++ /tmp/185-offline-enable.sh.XXXXKfCKND/config.ldif.nowrap
@@ -1,15 +1,3 @@
-# 
-# This file contains sensitive information, and it should not be shared
-# with untrusted individuals. The collect-support-data tool automatically
-# redacts this sensitive information when this file is shared with the
-# support team, and the tool also supports an --encrypt option to further 
-# protect this information in transit.
-# 
-# product=Ping Identity Directory Server
-# version=8.3.0.0
-# build-revision=29a2bc05
-# baseline-digest=A984E5BC
-# model-digest=85924BA9
 dn: cn=config
 objectClass: top
 objectClass: ds-cfg-root-config
185-offline-enable.sh: 2022-09-13 15:55:54 INFO Validate the descriptor.json syntax
185-offline-enable.sh: 2022-09-13 15:55:54 INFO Verifying descriptor.json content
{"us-east-2":{"hostname":"pingdirectory.ping-cloud.svc.cluster.local","replicas":3}}
185-offline-enable.sh: 2022-09-13 15:55:54 INFO local_region: us-east-2
185-offline-enable.sh: 2022-09-13 15:55:54 INFO local_hostname: pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:55:54 INFO local_count: 3
185-offline-enable.sh: 2022-09-13 15:55:54 INFO Deleting server groups: replication-servers all-servers
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Removing all existing server instances
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Creating top level server instance DN 'cn=Server Instances,cn=Topology,cn=config'
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Replacing local server instance name to 'cn=Server Instances,cn=Topology,cn=config'
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Updating existing replication entries for replication server DN 'cn=replication server,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config'
185-offline-enable.sh: 2022-09-13 15:55:55 INFO removing DNs no longer being replicated
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Updating existing replication domain o=platformconfig.
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Updating existing replication domain o=appintegrations.
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Updating existing replication domain dc=amstock,dc=com.
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Modifications being applied from /tmp/185-offline-enable.sh.XXXXKfCKND/mods.ldif LDIF file:
dn: cn=replication-servers,cn=Server Groups,cn=Topology,cn=config
changeType: delete

dn: cn=all-servers,cn=Server Groups,cn=Topology,cn=config
changeType: delete

dn: cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=5a4240c1-1db8-4af5-bd7d-747bf0329429,cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=b47a973f-a3a3-4175-9579-7b3fefa60e4c,cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=Server Instances,cn=Topology,cn=config
changeType: add
objectClass: ds-cfg-branch
objectClass: ds-mirrored-object
objectClass: top
cn: Server Instances
createTimestamp: 20220913155550.550Z

dn: cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: add
objectClass: ds-cfg-branch
objectClass: ds-mirrored-object
objectClass: top
objectClass: ds-cfg-server-instance
objectClass: ds-cfg-data-store-server-instance
cn: pingdirectory-0-us-east-2
ds-cfg-server-root: /opt/out/instance
ds-cfg-server-version: 8.3.0.0
ds-cfg-cluster-name: cluster_pingdirectory-0-us-east-2
ds-cfg-server-instance-name: pingdirectory-0-us-east-2
ds-cfg-inter-server-certificate:: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUN2akNDQWFZQ0NRQ3NMaEptdEYwQ3VEQU5CZ2txaGtpRzl3MEJBUXNGQURBZ01SNHdIQVlEVlFRRERCVnMKYjJOaGJHaHZjM1F1Ykc5allXeGtiMjFoYVc0d0lCY05NakF3TmpNd01UZ3hOekkwV2hnUE1qRXlNREEyTURZeApPREUzTWpSYU1DQXhIakFjQmdOVkJBTU1GV3h2WTJGc2FHOXpkQzVzYjJOaGJHUnZiV0ZwYmpDQ0FTSXdEUVlKCktvWklodmNOQVFFQkJRQURnZ0VQQURDQ0FRb0NnZ0VCQUtmalRHZVgweHhubG5LbXBodFB1Z21jRjNXRHREZmsKOUgyWGh4aXpsTzliNzhPWlk3ZGRxZXVpRktBU3ZZZEtzSE80cUVLMXhtMitvTHZaa2RIandFYlc5dVJYQ2Zucgo3cUpRaHpiemZpemtFOXE2MVBHazJTNGNlcytyUlBDZVlFSEUrd1J5bUdnMnNabXgrdVNLb1RvQk5lMnNnQ2lWCkw0YmpBZ3NKdkdxUzI2T0ZleTF6WTVRYXRmUkI0QlFKSis1eFJ3Z3BCSXdJOExRN3ozS0pkQlVyTll3TDlUemYKSVc2UjcxMHlORVhWWkxqa0pwemJTeGtub3kxQlc3SFJwYmxxNFZaWEFEWDNSYlpuV2xKRWhubkRBVGxPcWtregp5cHBUSnhvaEtkK0pZYXRFRUxWNC9DajkyR3UwcEJtSXorazkrWnJob3J1RTBkSHM2T0tlYStVQ0F3RUFBVEFOCkJna3Foa2lHOXcwQkFRc0ZBQU9DQVFFQVNVcUU1RUw1ZEttNDJWcmFEclpRM0prNXlTUUNtZE1HNGFoYmFndVUKNDk1aEV5NDlhNVhDL3NoS0hCUnJaVy95RTJiS1dTOTBKdzA2aVpUWkk0a3JXZnk5NUtxVlJhWkNYUHc4K0lWdwpLMjJZSTJ1MWVUNlpWYkpuL1dJL2VuMDBwNk1mRjhFTmF3STZTc081dzlVUnRhSFpRK2lhc1BSUERqeVljUC93CnNpbWlBeTB2a2hZSUM5Qmw1K0QxV3FwWm1PRnMvdW5EZC8xUFRxSXF5cHZINUcyYjBvUmdLTTUzQlBIZFBKajAKcEpObFBTblJFNThVNkM5RG5BcSt2cFlJZFE1UWdtQWVaMVA0T2E0cGdHY0NHNlBVYVRoalUxeFhFL01CQWFFRgpwV0pYT2pqWHUwdVpFbXE0bHFJakZEcmZDSkVISkliRmtzMUJjZVVQK3BkU2F3PT0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=
ds-cfg-server-instance-location: us-east-2
ds-cfg-hostname: pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
ds-cfg-replication-server-id: 1000
ds-cfg-ldap-port: 1389
ds-cfg-ldaps-port: 1636
ds-cfg-https-port: 1443
ds-cfg-replication-port: 8989
createTimestamp: 20220913155550.550Z
ds-cfg-replication-domain-server-id: 1001
ds-cfg-replication-domain-server-id: 1003
ds-cfg-replication-domain-server-id: 1005


dn: cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: add
objectClass: ds-cfg-branch
objectClass: ds-mirrored-object
objectClass: top
objectClass: ds-cfg-server-instance
objectClass: ds-cfg-data-store-server-instance
cn: pingdirectory-1-us-east-2
ds-cfg-server-root: /opt/out/instance
ds-cfg-server-version: 8.3.0.0
ds-cfg-cluster-name: cluster_pingdirectory-1-us-east-2
ds-cfg-server-instance-name: pingdirectory-1-us-east-2
ds-cfg-inter-server-certificate:: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUN2akNDQWFZQ0NRQ3NMaEptdEYwQ3VEQU5CZ2txaGtpRzl3MEJBUXNGQURBZ01SNHdIQVlEVlFRRERCVnMKYjJOaGJHaHZjM1F1Ykc5allXeGtiMjFoYVc0d0lCY05NakF3TmpNd01UZ3hOekkwV2hnUE1qRXlNREEyTURZeApPREUzTWpSYU1DQXhIakFjQmdOVkJBTU1GV3h2WTJGc2FHOXpkQzVzYjJOaGJHUnZiV0ZwYmpDQ0FTSXdEUVlKCktvWklodmNOQVFFQkJRQURnZ0VQQURDQ0FRb0NnZ0VCQUtmalRHZVgweHhubG5LbXBodFB1Z21jRjNXRHREZmsKOUgyWGh4aXpsTzliNzhPWlk3ZGRxZXVpRktBU3ZZZEtzSE80cUVLMXhtMitvTHZaa2RIandFYlc5dVJYQ2Zucgo3cUpRaHpiemZpemtFOXE2MVBHazJTNGNlcytyUlBDZVlFSEUrd1J5bUdnMnNabXgrdVNLb1RvQk5lMnNnQ2lWCkw0YmpBZ3NKdkdxUzI2T0ZleTF6WTVRYXRmUkI0QlFKSis1eFJ3Z3BCSXdJOExRN3ozS0pkQlVyTll3TDlUemYKSVc2UjcxMHlORVhWWkxqa0pwemJTeGtub3kxQlc3SFJwYmxxNFZaWEFEWDNSYlpuV2xKRWhubkRBVGxPcWtregp5cHBUSnhvaEtkK0pZYXRFRUxWNC9DajkyR3UwcEJtSXorazkrWnJob3J1RTBkSHM2T0tlYStVQ0F3RUFBVEFOCkJna3Foa2lHOXcwQkFRc0ZBQU9DQVFFQVNVcUU1RUw1ZEttNDJWcmFEclpRM0prNXlTUUNtZE1HNGFoYmFndVUKNDk1aEV5NDlhNVhDL3NoS0hCUnJaVy95RTJiS1dTOTBKdzA2aVpUWkk0a3JXZnk5NUtxVlJhWkNYUHc4K0lWdwpLMjJZSTJ1MWVUNlpWYkpuL1dJL2VuMDBwNk1mRjhFTmF3STZTc081dzlVUnRhSFpRK2lhc1BSUERqeVljUC93CnNpbWlBeTB2a2hZSUM5Qmw1K0QxV3FwWm1PRnMvdW5EZC8xUFRxSXF5cHZINUcyYjBvUmdLTTUzQlBIZFBKajAKcEpObFBTblJFNThVNkM5RG5BcSt2cFlJZFE1UWdtQWVaMVA0T2E0cGdHY0NHNlBVYVRoalUxeFhFL01CQWFFRgpwV0pYT2pqWHUwdVpFbXE0bHFJakZEcmZDSkVISkliRmtzMUJjZVVQK3BkU2F3PT0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=
ds-cfg-server-instance-location: us-east-2
ds-cfg-hostname: pingdirectory-1.pingdirectory.ping-cloud.svc.cluster.local
ds-cfg-replication-server-id: 1100
ds-cfg-ldap-port: 1389
ds-cfg-ldaps-port: 1636
ds-cfg-https-port: 1443
ds-cfg-replication-port: 8989
createTimestamp: 20220913155550.550Z
ds-cfg-replication-domain-server-id: 1101
ds-cfg-replication-domain-server-id: 1103
ds-cfg-replication-domain-server-id: 1105


dn: cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: add
objectClass: ds-cfg-branch
objectClass: ds-mirrored-object
objectClass: top
objectClass: ds-cfg-server-instance
objectClass: ds-cfg-data-store-server-instance
cn: pingdirectory-2-us-east-2
ds-cfg-server-root: /opt/out/instance
ds-cfg-server-version: 8.3.0.0
ds-cfg-cluster-name: cluster_pingdirectory-2-us-east-2
ds-cfg-server-instance-name: pingdirectory-2-us-east-2
ds-cfg-inter-server-certificate:: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUN2akNDQWFZQ0NRQ3NMaEptdEYwQ3VEQU5CZ2txaGtpRzl3MEJBUXNGQURBZ01SNHdIQVlEVlFRRERCVnMKYjJOaGJHaHZjM1F1Ykc5allXeGtiMjFoYVc0d0lCY05NakF3TmpNd01UZ3hOekkwV2hnUE1qRXlNREEyTURZeApPREUzTWpSYU1DQXhIakFjQmdOVkJBTU1GV3h2WTJGc2FHOXpkQzVzYjJOaGJHUnZiV0ZwYmpDQ0FTSXdEUVlKCktvWklodmNOQVFFQkJRQURnZ0VQQURDQ0FRb0NnZ0VCQUtmalRHZVgweHhubG5LbXBodFB1Z21jRjNXRHREZmsKOUgyWGh4aXpsTzliNzhPWlk3ZGRxZXVpRktBU3ZZZEtzSE80cUVLMXhtMitvTHZaa2RIandFYlc5dVJYQ2Zucgo3cUpRaHpiemZpemtFOXE2MVBHazJTNGNlcytyUlBDZVlFSEUrd1J5bUdnMnNabXgrdVNLb1RvQk5lMnNnQ2lWCkw0YmpBZ3NKdkdxUzI2T0ZleTF6WTVRYXRmUkI0QlFKSis1eFJ3Z3BCSXdJOExRN3ozS0pkQlVyTll3TDlUemYKSVc2UjcxMHlORVhWWkxqa0pwemJTeGtub3kxQlc3SFJwYmxxNFZaWEFEWDNSYlpuV2xKRWhubkRBVGxPcWtregp5cHBUSnhvaEtkK0pZYXRFRUxWNC9DajkyR3UwcEJtSXorazkrWnJob3J1RTBkSHM2T0tlYStVQ0F3RUFBVEFOCkJna3Foa2lHOXcwQkFRc0ZBQU9DQVFFQVNVcUU1RUw1ZEttNDJWcmFEclpRM0prNXlTUUNtZE1HNGFoYmFndVUKNDk1aEV5NDlhNVhDL3NoS0hCUnJaVy95RTJiS1dTOTBKdzA2aVpUWkk0a3JXZnk5NUtxVlJhWkNYUHc4K0lWdwpLMjJZSTJ1MWVUNlpWYkpuL1dJL2VuMDBwNk1mRjhFTmF3STZTc081dzlVUnRhSFpRK2lhc1BSUERqeVljUC93CnNpbWlBeTB2a2hZSUM5Qmw1K0QxV3FwWm1PRnMvdW5EZC8xUFRxSXF5cHZINUcyYjBvUmdLTTUzQlBIZFBKajAKcEpObFBTblJFNThVNkM5RG5BcSt2cFlJZFE1UWdtQWVaMVA0T2E0cGdHY0NHNlBVYVRoalUxeFhFL01CQWFFRgpwV0pYT2pqWHUwdVpFbXE0bHFJakZEcmZDSkVISkliRmtzMUJjZVVQK3BkU2F3PT0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=
ds-cfg-server-instance-location: us-east-2
ds-cfg-hostname: pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
ds-cfg-replication-server-id: 1200
ds-cfg-ldap-port: 1389
ds-cfg-ldaps-port: 1636
ds-cfg-https-port: 1443
ds-cfg-replication-port: 8989
createTimestamp: 20220913155550.550Z
ds-cfg-replication-domain-server-id: 1201
ds-cfg-replication-domain-server-id: 1203
ds-cfg-replication-domain-server-id: 1205


dn: cn=config
changeType: modify
replace: ds-cfg-instance-name
ds-cfg-instance-name: pingdirectory-0-us-east-2


dn: cn=replication server,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-replication-server-id
ds-cfg-replication-server-id: 1000
-
replace: ds-cfg-replication-port
ds-cfg-replication-port: 8989


dn: cn=o_platformconfig,cn=domains,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-server-id
ds-cfg-server-id: 1001
-
replace: cn
cn: o_platformconfig
-
replace: ds-cfg-base-dn
ds-cfg-base-dn: o=platformconfig

dn: cn=o_appintegrations,cn=domains,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-server-id
ds-cfg-server-id: 1003
-
replace: cn
cn: o_appintegrations
-
replace: ds-cfg-base-dn
ds-cfg-base-dn: o=appintegrations

dn: cn=dc_amstock_dc_com,cn=domains,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-server-id
ds-cfg-server-id: 1005
-
replace: cn
cn: dc_amstock_dc_com
-
replace: ds-cfg-base-dn
ds-cfg-base-dn: dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:55:55 INFO Calling ldifmodify for mods '/tmp/185-offline-enable.sh.XXXXKfCKND/mods.ldif'
Successfully completed processing.  Source entries read:  707.  Entries
updated:  19.  Entries not updated:  688.
185-offline-enable.sh: 2022-09-13 15:55:56 INFO There are no zero (unused) ports in /opt/out/instance/config/config.ldif.
185-offline-enable.sh: 2022-09-13 15:55:56 INFO Admin user 'admin' already exists.
185-offline-enable.sh: 2022-09-13 15:55:56 INFO group 'replication-servers' does not already exist - creating
185-offline-enable.sh: 2022-09-13 15:55:56 INFO Creating 'replication-servers' group with members:  pingdirectory-0-us-east-2 pingdirectory-1-us-east-2 pingdirectory-2-us-east-2.
185-offline-enable.sh: 2022-09-13 15:55:56 INFO group 'all-servers' does not already exist - creating
185-offline-enable.sh: 2022-09-13 15:55:56 INFO Creating 'all-servers' group with members:  pingdirectory-0-us-east-2 pingdirectory-1-us-east-2 pingdirectory-2-us-east-2.
185-offline-enable.sh: 2022-09-13 15:55:56 INFO applying dsconfig from file /tmp/185-offline-enable.sh.XXXXKfCKND/batch.dsconfig:
dsconfig create-server-group \
  --group-name "replication-servers" \
   --set member:pingdirectory-0-us-east-2 --set member:pingdirectory-1-us-east-2 --set member:pingdirectory-2-us-east-2

dsconfig create-server-group \
  --group-name "all-servers" \
   --set member:pingdirectory-0-us-east-2 --set member:pingdirectory-1-us-east-2 --set member:pingdirectory-2-us-east-2

[13/Sep/2022:15:55:58 +0000] SEVERE_WARNING The Directory Server has sent an alert notification generated by class com.unboundid.directory.server.extensions.ConfigFileHandler (alert type offline-config-change-detected, alert ID 835326df-8d0a-4962-aa52-de92867c900b):  The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913155449Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=all-servers,cn=Server Groups,cn=topology,cn=config', 'cn=replication-servers,cn=Server Groups,cn=topology,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=b47a973f-a3a3-4175-9579-7b3fefa60e4c,cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=5a4240c1-1db8-4af5-bd7d-747bf0329429,cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config'
[13/Sep/2022:15:56:02 +0000] SEVERE_WARNING The Directory Server has sent an alert notification generated by class com.unboundid.directory.server.extensions.ConfigFileHandler (alert type offline-config-change-detected, alert ID 076045a5-c716-400e-85ff-b208b113a0a8):  The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913155449Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=all-servers,cn=Server Groups,cn=topology,cn=config', 'cn=replication-servers,cn=Server Groups,cn=topology,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=b47a973f-a3a3-4175-9579-7b3fefa60e4c,cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=5a4240c1-1db8-4af5-bd7d-747bf0329429,cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config'

Arguments from tool properties file:  --useSSL  --hostname localhost --port
1636 --bindDN cn=administrator --bindPasswordFile
/usr/local/secrets/root-user-password --trustAll

Batch file '/tmp/185-offline-enable.sh.XXXXKfCKND/batch.dsconfig' contains 2 commands.

Pre-validating with the local server ..... Done

Executing: create-server-group --no-prompt --offline --skipOfflineAuditLogging
--group-name replication-servers --set member:pingdirectory-0-us-east-2 --set
member:pingdirectory-1-us-east-2 --set member:pingdirectory-2-us-east-2

Arguments from tool properties file:  --useSSL  --hostname localhost --port
1636 --bindDN cn=administrator --bindPasswordFile
/usr/local/secrets/root-user-password --trustAll


The Server Group was created successfully

Executing: create-server-group --no-prompt --offline --skipOfflineAuditLogging
--group-name all-servers --set member:pingdirectory-0-us-east-2 --set
member:pingdirectory-1-us-east-2 --set member:pingdirectory-2-us-east-2

Arguments from tool properties file:  --useSSL  --hostname localhost --port
1636 --bindDN cn=administrator --bindPasswordFile
/usr/local/secrets/root-user-password --trustAll


The Server Group was created successfully

185-offline-enable.sh: 2022-09-13 15:56:09 INFO restoring the original header
185-offline-enable.sh: 2022-09-13 15:56:09 INFO End for '/opt/out/instance'
185-offline-enable-wrapper.sh: 2022-09-13 15:56:09 INFO offline enable complete
20-restart-sequence.sh: 2022-09-13 15:56:09 INFO offline replication enable status: 0
20-restart-sequence.sh: 2022-09-13 15:56:09 INFO restart sequence done


----- Starting hook: /opt/staging/hooks/50-before-post-start.sh

Starting server in foreground: (/opt/out/instance/bin/start-server --nodetach)

----- Starting hook: /opt/staging/hooks/80-post-start.sh
80-post-start.sh: 2022-09-13 15:56:09 INFO export config settings
80-post-start.sh: 2022-09-13 15:56:09 INFO MULTI_CLUSTER - false
80-post-start.sh: 2022-09-13 15:56:09 INFO PRIMARY_CLUSTER - true
80-post-start.sh: 2022-09-13 15:56:09 INFO PD_HTTPS_PORT - 1443
80-post-start.sh: 2022-09-13 15:56:09 INFO PD_LDAP_PORT - 1389
80-post-start.sh: 2022-09-13 15:56:09 INFO PD_LDAPS_PORT - 1636
80-post-start.sh: 2022-09-13 15:56:09 INFO PD_REPL_PORT - 8989
80-post-start.sh: 2022-09-13 15:56:09 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
80-post-start.sh: 2022-09-13 15:56:09 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
80-post-start.sh: 2022-09-13 15:56:09 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
80-post-start.sh: 2022-09-13 15:56:09 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
80-post-start.sh: 2022-09-13 15:56:09 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
80-post-start.sh: 2022-09-13 15:56:09 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
80-post-start.sh: 2022-09-13 15:56:09 INFO starting post-start hook
80-post-start.sh: 2022-09-13 15:56:09 INFO running ldapsearch test on this container (pingdirectory-0)
Sleeping 1 seconds (max: 15)...
Sleeping 14 seconds (max: 15)...
2022-09-13T15:56:15,010+0000 [17 1] com.newrelic INFO: New Relic Agent: Loading configuration file "/opt/shared-dir/newrelic.yml"
2022-09-13T15:56:15,075+0000 [17 1] com.newrelic INFO: Using default collector host: collector.newrelic.com
2022-09-13T15:56:15,151+0000 [17 1] com.newrelic INFO: New Relic Agent: Writing to log file: /opt/staging/logs/newrelic_agent.log
WARNING: An illegal reflective access operation has occurred
WARNING: Illegal reflective access by com.newrelic.weave.weavepackage.NewClassAppender (file:/opt/staging/newrelic.jar) to method java.net.URLClassLoader.addURL(java.net.URL)
WARNING: Please consider reporting this to the maintainers of com.newrelic.weave.weavepackage.NewClassAppender
WARNING: Use --illegal-access=warn to enable warnings of further illegal reflective access operations
WARNING: All illegal access operations will be denied in a future release



********************************************************************************
[13/Sep/2022:15:56:21.575 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=dd866da7-1012-4250-b875-d2713844caf3 class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913155449Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=b47a973f-a3a3-4175-9579-7b3fefa60e4c,cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=5a4240c1-1db8-4af5-bd7d-747bf0329429,cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



[13/Sep/2022:15:56:23.201 +0000] category=CORE severity=NOTICE msgID=458886 msg="Ping Identity Directory Server 8.3.0.0 (build 20210618165156Z, Rv8.3.0.0-GA) starting up"



********************************************************************************
[13/Sep/2022:15:56:24.625 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3277462 msg="Schema configuration file 50-AST-DIT.ldif in directory /opt/out/instance/config/schema contains more than one entry.  Only the first entry will be examined, and the additional entries will be ignored"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:24.626 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3277462 msg="Schema configuration file 52-AdminGroups.ldif in directory /opt/out/instance/config/schema contains more than one entry.  Only the first entry will be examined, and the additional entries will be ignored"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:24.633 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276992 msg="Schema configuration file 53-AST-ACI.ldif in directory /opt/out/instance/config/schema cannot be parsed because an unexpected error occurred while trying to read its contents as an LDIF entry:  Unable to parse LDIF entry starting at line 1 because the line '-' does not include an attribute name (id=5439494 LDIFReader.java:2007 8.3.0.0-20210617212340.000Z-29a2bc05)"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:24.634 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3277462 msg="Schema configuration file 54-AST-Dev-Test-Users_20210920.ldif in directory /opt/out/instance/config/schema contains more than one entry.  Only the first entry will be examined, and the additional entries will be ignored"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:24.635 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276992 msg="Schema configuration file 61-RemovePermissiveACI.ldif in directory /opt/out/instance/config/schema cannot be parsed because an unexpected error occurred while trying to read its contents as an LDIF entry:  Unable to parse LDIF entry starting at line 2 because the line '-' does not include an attribute name (id=5439494 LDIFReader.java:2007 8.3.0.0-20210617212340.000Z-29a2bc05)"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:24.635 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276992 msg="Schema configuration file 62-ModPwdState.ldif in directory /opt/out/instance/config/schema cannot be parsed because an unexpected error occurred while trying to read its contents as an LDIF entry:  Unable to parse LDIF entry starting at line 1 because the line '-' does not include an attribute name (id=5439494 LDIFReader.java:2007 8.3.0.0-20210617212340.000Z-29a2bc05)"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:24.675 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276995 msg="An objectclass read from schema configuration file 98-ast.ldif conflicts with another objectclass already read into the schema:  Unable to register object class 'astUser' with the server schema because its OID 'astuser-oid' conflicts with the OID of an existing object class 'astUser'.  The later objectclass definition will be used"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:24.806 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=0e093390-a080-44bf-9d10-fd40b7fa02af class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913155449Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=b47a973f-a3a3-4175-9579-7b3fefa60e4c,cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=5a4240c1-1db8-4af5-bd7d-747bf0329429,cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



[13/Sep/2022:15:56:25.143 +0000] category=CORE severity=NOTICE msgID=1879508001 msg="The third-party extension class com.pingidentity.pingcloud.pingdatasdk.pingdirectory.P14CPassThroughPreParsePlugin, version 1.0.2, has been loaded into the server using the configuration defined in cn=PingOne for Customers Pass-Through Authentication Pre-Parse Plugin,cn=Plugins,cn=config"



********************************************************************************
[13/Sep/2022:15:56:28.393 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=dd866da7-1012-4250-b875-d2713844caf3 class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913155449Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=b47a973f-a3a3-4175-9579-7b3fefa60e4c,cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=5a4240c1-1db8-4af5-bd7d-747bf0329429,cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:28.394 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=0e093390-a080-44bf-9d10-fd40b7fa02af class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913155449Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=b47a973f-a3a3-4175-9579-7b3fefa60e4c,cn=Cipher Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=5a4240c1-1db8-4af5-bd7d-747bf0329429,cn=MAC Secret Keys,cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



[13/Sep/2022:15:56:28.410 +0000] category=EXTENSIONS severity=NOTICE msgID=1880555611 msg="Administrative alert type=server-starting id=e1fdf9f0-921e-4795-96b2-ab8e998b0915 class=com.unboundid.directory.server.core.DirectoryServer msg='The Directory Server is starting'"
Sleeping 8 seconds (max: 15)...
[13/Sep/2022:15:56:31.690 +0000] category=JEB severity=NOTICE msgID=1887895580 msg="Starting cache priming for 67 databases in backend appintegrations"
[13/Sep/2022:15:56:31.743 +0000] category=JEB severity=NOTICE msgID=1887896003 msg="Preloaded 49 entry records and 668 index records (96% embedded within internal database structure) in 0 seconds"
[13/Sep/2022:15:56:31.748 +0000] category=JEB severity=NOTICE msgID=1887895587 msg="The database cache now holds 115MB of data and is 24 percent full"
[13/Sep/2022:15:56:32.127 +0000] category=CONFIG severity=NOTICE msgID=1882652783 msg="Initializing mirrored topology and cluster-wide configuration"
[13/Sep/2022:15:56:32.874 +0000] category=JEB severity=NOTICE msgID=1887895580 msg="Starting cache priming for 36 databases in backend platformconfig"
[13/Sep/2022:15:56:32.883 +0000] category=JEB severity=NOTICE msgID=1887896003 msg="Preloaded 41 entry records and 1315 index records (95% embedded within internal database structure) in 0 seconds"
[13/Sep/2022:15:56:32.885 +0000] category=JEB severity=NOTICE msgID=1887895587 msg="The database cache now holds 3MB of data and is 2 percent full"



********************************************************************************
[13/Sep/2022:15:56:33.101 +0000] category=CONFIG severity=SEVERE_WARNING msgID=1882325089 msg="Backend 'userRoot' is configured with multiple base DNs.  While this is currently supported, this capability should be considered deprecated and may be removed in the future.  Configuring a backend with multiple base DNs may introduce complexity in replication (where some features like online initialization via binary copy may not be available) or other areas and is not recommended.  This warning may be disabled via the warn-for-multiple-base-dns global configuration property, but it is strongly recommended that you first contact Ping Identity support to discuss the use of multiple base DNs in your directory environment"
********************************************************************************



Sleeping 5 seconds (max: 15)...
Sleeping 10 seconds (max: 15)...
[13/Sep/2022:15:56:46.186 +0000] category=CORE severity=NOTICE msgID=1879507304 msg="Invoking an explicit garbage collection because backend initialization took longer than 17560 milliseconds, which is greater than the forced-gc-prime-duration of 10000 milliseconds (maxMemory=3221225472, allocatedMemory=3221225472, usedMemory=525992016, freeMemory=2695233456)"
[13/Sep/2022:15:56:46.424 +0000] category=CORE severity=NOTICE msgID=1879507305 msg="Explicit garbage collection completed after 238 milliseconds (maxMemory=3221225472, allocatedMemory=3221225472, usedMemory=525992016, freeMemory=2900527168)"
[13/Sep/2022:15:56:46.424 +0000] category=CORE severity=NOTICE msgID=1879508187 msg="Startup timing: 11.733 seconds for 'Recovering recent changes for backend changelog'"



********************************************************************************
[13/Sep/2022:15:56:46.455 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=debug-logging-enabled id=9ccf0091-034b-496d-bf39-012ad9fa230b class=com.unboundid.directory.server.loggers.debug.TextDebugLogPublisher msg='A Debug Log Publisher is enabled. When Debug Targets are configured to restrict what is logged, the performance impact is typically negligible. However, it is good practice to disable the Debug Log Publisher once the required information has been collected'"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:56:46.463 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=no-enabled-alert-handlers id=78e287f9-a0f5-485d-b802-0bd4ff312fab class=com.unboundid.directory.server.core.AlertHandlerConfigManager msg='No alert handlers have been enabled. Alerts will be written to logs/errors, but administrators will not be otherwise notified of current or impending problems. The server uses alerts to self-report many problems or precursors to potential problems. If an administrator does not receive these alerts, then there might be a server outage that was avoidable. In production environments, we strongly recommend enabling the SMTP Alert Handler to send emails, the JMX or SNMP Alert Handler to send notifications to a monitoring application, or creating a custom alert handler. In non-product environments, this alarm can be suppressed by adding 'no-enabled-alert-handlers' to the 'suppressed-alarm' configuration property on the Alarm Manager configuration object'"
********************************************************************************



[13/Sep/2022:15:56:47.564 +0000] category=PROTOCOL severity=NOTICE msgID=1881604184 msg="HTTP Connection Handler HTTPS Connection Handler using 8 threads"
[13/Sep/2022:15:56:52.630 +0000] category=CORE severity=NOTICE msgID=1879508001 msg="The third-party extension class com.pingidentity.ps.pd.plugin.ast.SessionRevocationAccountStatusNotificationHandler, version 1.0.1, has been loaded into the server using the configuration defined in cn=Session Revocation Notification Handler,cn=Account Status Notification Handlers,cn=config"
[13/Sep/2022:15:56:53.090 +0000] category=EXTENSIONS severity=NOTICE msgID=1880556375 msg="Successfully set the delegated admin ACI"



********************************************************************************
[13/Sep/2022:15:56:53.116 +0000] category=EXTENSIONS severity=SEVERE_ERROR msgID=1880359005 msg="Administrative alert type=delegated-admin-configuration-errors id=3a303a9b-3ad4-4e81-9820-b7673e3c1cb8 class=com.unboundid.directory.server.extensions.dadmin.DelegatedAdminAlertGenerator msg='The Delegated Admin configuration has the following errors: Delegated Admin Rights 'administrator-user-dadmin' Admin User DN 'uid=admin,dc=amstock,dc=com' references a nonexistent entry'"
********************************************************************************



Sleeping 5 seconds (max: 15)...
Sleeping 3 seconds (max: 15)...
[13/Sep/2022:15:57:04.327 +0000] category=REPLICATION severity=NOTICE msgID=118947974 msg="The replication server startup min replication backlog count is 5000"
[13/Sep/2022:15:57:04.339 +0000] category=REPLICATION severity=NOTICE msgID=118947923 msg="Replication server startup min replication backlog processing completed. All local replicas available when the server was started have reported below the configured threshold of 5000"
[13/Sep/2022:15:57:04.348 +0000] category=CORE severity=NOTICE msgID=1879508187 msg="Startup timing: 11.303 seconds for 'Initializing Plugins'"



********************************************************************************
[13/Sep/2022:15:57:06.177 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880228292 msg="The Linux kernel parameter vm.swappiness is set to '60' instead of '0'.  This non-zero setting allows Linux to swap temporarily inactive parts of the JVM out of memory to disk.  When the JVM later accesses large amounts of this swapped out memory (for instance during a garbage collection cycle), the server can experience pauses of several seconds where no processing occurs.  We strongly recommend setting this value to '0' by executing 'sysctl -w vm.swappiness=0' as root to change the current value in the operating system and by adding a line 'vm.swappiness = 0' to /etc/sysctl.conf to ensure that the correct setting is applied when the system restarts. If a system performance service such as tuned is used, also apply the vm.swappiness setting to the active profile or disable the service. To check for an active performance profile run the tuned-adm active command"
********************************************************************************



[13/Sep/2022:15:57:06.200 +0000] category=CORE severity=NOTICE msgID=1879507495 msg="One or more third-party extensions have been loaded into the server.  The DNs of the configuration entries for the third-party extensions are:  'cn=Session Revocation Notification Handler,cn=Account Status Notification Handlers,cn=config', 'cn=PingOne for Customers Pass-Through Authentication Pre-Parse Plugin,cn=Plugins,cn=config'"
[13/Sep/2022:15:57:06.200 +0000] category=CORE severity=NOTICE msgID=458887 msg="The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully"
[13/Sep/2022:15:57:06.200 +0000] category=EXTENSIONS severity=NOTICE msgID=1880555611 msg="Administrative alert type=server-started id=43b0bdd1-0439-4ad4-8d2b-4e627daca442 class=com.unboundid.directory.server.core.DirectoryServer msg='The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully'"
dn: cn=config

80-post-start.sh: 2022-09-13 15:57:09 INFO pod ordinal: 0; multi-cluster: false
80-post-start.sh: 2022-09-13 15:57:09 INFO resetting password for user DN: uid=administrator,ou=admins,o=platformconfig

# Password Modify Extended Result:
# Result Code:  53 (unwilling to perform)
# Diagnostic Message:  The provided new password cannot be the same as the
#      current password or any password in the password history

The password modify extended operation failed with result code 53 (unwilling to
perform) and diagnostic message The provided new password cannot be the same as
the current password or any password in the password history
80-post-start.sh: 2022-09-13 15:S57:11 INFO password reset for DN uid=administrator,ou=admins,o=platformconfig status: 53
80-post-start.sh: 2022-09-13 15:57:11 INFO resetting password for user DN: uid=pingfederate,ou=devopsaccount,o=platformconfig

# Password Modify Extended Result:
The password modify extended operation failed with result code 53 (unwilling to
perform) and diagnostic message The provided new password cannot be the same as
the current password or any password in the password history
# Result Code:  53 (unwilling to perform)
# Diagnostic Message:  The provided new password cannot be the same as the
#      current password or any password in the password history

80-post-start.sh: 2022-09-13 15:57:14 INFO password reset for DN uid=pingfederate,ou=devopsaccount,o=platformconfig status: 53
80-post-start.sh: 2022-09-13 15:57:14 INFO resetting password for user DN: cn=admin

# Password Modify Extended Result:
The password modify extended operation failed with result code 53 (unwilling to
perform) and diagnostic message The provided new password cannot be the same as
the current password or any password in the password history
# Result Code:  53 (unwilling to perform)
# Diagnostic Message:  The provided new password cannot be the same as the
#      current password or any password in the password history

80-post-start.sh: 2022-09-13 15:57:16 INFO password reset for DN cn=admin status: 53
80-post-start.sh: 2022-09-13 15:57:16 INFO not initializing replication data because INITIALIZE_REPLICATION_DATA is false
80-post-start.sh: 2022-09-13 15:57:16 INFO post-start complete

----- Starting hook: /opt/staging/hooks/100-tail-logs.sh
100-tail-logs.sh: 2022-09-13 15:57:16 INFO export config settings
100-tail-logs.sh: 2022-09-13 15:57:16 INFO MULTI_CLUSTER - false
100-tail-logs.sh: 2022-09-13 15:57:16 INFO PRIMARY_CLUSTER - true
100-tail-logs.sh: 2022-09-13 15:57:16 INFO PD_HTTPS_PORT - 1443
100-tail-logs.sh: 2022-09-13 15:57:16 INFO PD_LDAP_PORT - 1389
100-tail-logs.sh: 2022-09-13 15:57:16 INFO PD_LDAPS_PORT - 1636
100-tail-logs.sh: 2022-09-13 15:57:16 INFO PD_REPL_PORT - 8989
100-tail-logs.sh: 2022-09-13 15:57:16 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
100-tail-logs.sh: 2022-09-13 15:57:16 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
100-tail-logs.sh: 2022-09-13 15:57:16 INFO LOCAL_HOST_NAME - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
100-tail-logs.sh: 2022-09-13 15:57:16 INFO LOCAL_INSTANCE_NAME - pingdirectory-0-us-east-2
100-tail-logs.sh: 2022-09-13 15:57:16 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
100-tail-logs.sh: 2022-09-13 15:57:16 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
100-tail-logs.sh: 2022-09-13 15:57:16 INFO Tailing logs: /opt/out/instance/logs/access /opt/out/instance/logs/change-notifications.log /opt/out/instance/logs/errors /opt/out/instance/logs/failed-ops /opt/out/instance/logs/expensive-write-ops /opt/out/instance/logs/replication


/opt/out/instance/logs/expensive-write-ops # Logger shut down at 12/Sep/2022:19:47:31 +0000
/opt/out/instance/logs/expensive-write-ops # Logger initialized at 12/Sep/2022:19:48:45 +0000
/opt/out/instance/logs/expensive-write-ops # Logger shut down at 12/Sep/2022:22:04:36 +0000
/opt/out/instance/logs/expensive-write-ops # Logger initialized at 12/Sep/2022:22:07:31 +0000
/opt/out/instance/logs/expensive-write-ops # Logger shut down at 12/Sep/2022:22:07:56 +0000
/opt/out/instance/logs/expensive-write-ops # Logger initialized at 12/Sep/2022:22:09:09 +0000
/opt/out/instance/logs/expensive-write-ops # Logger shut down at 13/Sep/2022:15:51:58 +0000
/opt/out/instance/logs/expensive-write-ops # Logger initialized at 13/Sep/2022:15:54:53 +0000
/opt/out/instance/logs/expensive-write-ops # Logger shut down at 13/Sep/2022:15:55:12 +0000
/opt/out/instance/logs/expensive-write-ops # Logger initialized at 13/Sep/2022:15:56:28 +0000
/opt/out/instance/logs/access [13/Sep/2022:15:57:14.958 +0000] SECURITY-NEGOTIATION requesterIP="127.0.0.1" instanceName="pingdirectory-0-us-east-2" threadID=376 conn=4 protocol="TLSv1.3" cipher="TLS_AES_256_GCM_SHA384" clientServerHandshakeTimeMillis="107.478" serverOnlyHandshakeTimeMillis="24.959"
/opt/out/instance/logs/access [13/Sep/2022:15:57:15.001 +0000] BIND RESULT instanceName="pingdirectory-0-us-east-2" threadID=11 conn=4 op=0 msgID=1 requesterIP="127.0.0.1" version="3" dn="cn=administrator" authType="SIMPLE" resultCode=0 resultCodeName="Success" qtime=0 etime=16.333 authDN="cn=Directory Manager,cn=Root DNs,cn=config" clientConnectionPolicy="default"
/opt/out/instance/logs/access [13/Sep/2022:15:57:15.029 +0000] SEARCH RESULT instanceName="pingdirectory-0-us-east-2" threadID=10 conn=4 op=1 msgID=2 requesterIP="127.0.0.1" requesterDN="cn=Directory Manager,cn=Root DNs,cn=config" base="cn=monitor" scope=2 filter="(objectClass=ds-replication-server-summary-monitor-entry)" attrs="replica,replication-server" resultCode=0 resultCodeName="Success" qtime=0 etime=12.798 usedPrivileges="bypass-acl" entriesReturned=3
/opt/out/instance/logs/access [13/Sep/2022:15:57:15.084 +0000] DISCONNECT requesterIP="127.0.0.1" requesterDN="cn=Directory Manager,cn=Root DNs,cn=config" instanceName="pingdirectory-0-us-east-2" threadID=376 conn=4 reason="Client Unbind"
/opt/out/instance/logs/access [13/Sep/2022:15:57:16.054 +0000] CONNECT instanceName="pingdirectory-0-us-east-2" threadID=552 conn=5 from="127.0.0.1" fromPort=36664 to="127.0.0.1" toPort=1636 protocol="LDAP+TLS" clientConnectionPolicy="default"
/opt/out/instance/logs/access [13/Sep/2022:15:57:16.239 +0000] SECURITY-NEGOTIATION requesterIP="127.0.0.1" instanceName="pingdirectory-0-us-east-2" threadID=377 conn=5 protocol="TLSv1.3" cipher="TLS_AES_256_GCM_SHA384" clientServerHandshakeTimeMillis="74.300" serverOnlyHandshakeTimeMillis="20.406"
/opt/out/instance/logs/access [13/Sep/2022:15:57:16.284 +0000] BIND RESULT instanceName="pingdirectory-0-us-east-2" threadID=11 conn=5 op=0 msgID=1 requesterIP="127.0.0.1" version="3" dn="cn=administrator" authType="SIMPLE" resultCode=0 resultCodeName="Success" qtime=0 etime=17.358 authDN="cn=Directory Manager,cn=Root DNs,cn=config" clientConnectionPolicy="default"
/opt/out/instance/logs/access [13/Sep/2022:15:57:16.313 +0000] SEARCH RESULT instanceName="pingdirectory-0-us-east-2" threadID=10 conn=5 op=1 msgID=2 requesterIP="127.0.0.1" requesterDN="cn=Directory Manager,cn=Root DNs,cn=config" base="" scope=0 filter="(objectClass=*)" attrs="*,+,altServer,changelog,firstChangeNumber,lastChangeNumber,lastPurgedChangeNumber,namingContexts,subschemaSubentry,supportedAuthPasswordSchemes,supportedControl,supportedExtension,supportedFeatures,supportedLDAPVersion,supportedSASLMechanisms,vendorName,vendorVersion" resultCode=0 resultCodeName="Success" qtime=0 etime=1.298 usedPrivileges="bypass-acl" entriesReturned=1
/opt/out/instance/logs/access [13/Sep/2022:15:57:16.339 +0000] EXTENDED RESULT instanceName="pingdirectory-0-us-east-2" threadID=11 conn=5 op=2 msgID=3 requesterIP="127.0.0.1" requesterDN="cn=Directory Manager,cn=Root DNs,cn=config" requestControls="1.3.6.1.4.1.30221.2.5.51" requestOID="1.3.6.1.4.1.4203.1.11.1" requestType="Password Modify" resultCode=53 resultCodeName="Unwilling to Perform" message="The provided new password cannot be the same as the current password or any password in the password history" qtime=0 etime=11.892 usedPrivileges="bypass-acl,password-reset" passwordUpdateBehaviorAllowPreEncodedPassword="true" targetEntry="cn=admin,cn=Topology Admin Users,cn=topology,cn=config"
/opt/out/instance/logs/access [13/Sep/2022:15:57:16.352 +0000] DISCONNECT requesterIP="127.0.0.1" requesterDN="cn=Directory Manager,cn=Root DNs,cn=config" instanceName="pingdirectory-0-us-east-2" threadID=377 conn=5 reason="Client Unbind"
/opt/out/instance/logs/errors [13/Sep/2022:15:56:59.377 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=15138878 msg="Connected to server pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local:8989 for dc=amstock,dc=com [id: 1000]"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:04.221 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=15138878 msg="Connected to server pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local:8989 for o=appintegrations [id: 1000]"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:04.266 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=15138878 msg="Connected to server pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local:8989 for o=platformconfig [id: 1000]"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:04.328 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=118947974 msg="The replication server startup min replication backlog count is 5000"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:04.339 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=118947923 msg="Replication server startup min replication backlog processing completed. All local replicas available when the server was started have reported below the configured threshold of 5000"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:04.348 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=CORE severity=NOTICE msgID=1879508187 msg="Startup timing: 11.303 seconds for 'Initializing Plugins'"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:06.177 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=EXTENSIONS severity=SEVERE_WARNING msgID=1880228292 msg="The Linux kernel parameter vm.swappiness is set to '60' instead of '0'.  This non-zero setting allows Linux to swap temporarily inactive parts of the JVM out of memory to disk.  When the JVM later accesses large amounts of this swapped out memory (for instance during a garbage collection cycle), the server can experience pauses of several seconds where no processing occurs.  We strongly recommend setting this value to '0' by executing 'sysctl -w vm.swappiness=0' as root to change the current value in the operating system and by adding a line 'vm.swappiness = 0' to /etc/sysctl.conf to ensure that the correct setting is applied when the system restarts. If a system performance service such as tuned is used, also apply the vm.swappiness setting to the active profile or disable the service. To check for an active performance profile run the tuned-adm active command"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:06.200 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=CORE severity=NOTICE msgID=1879507495 msg="One or more third-party extensions have been loaded into the server.  The DNs of the configuration entries for the third-party extensions are:  'cn=Session Revocation Notification Handler,cn=Account Status Notification Handlers,cn=config', 'cn=PingOne for Customers Pass-Through Authentication Pre-Parse Plugin,cn=Plugins,cn=config'"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:06.200 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=CORE severity=NOTICE msgID=458887 msg="The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully"
/opt/out/instance/logs/errors [13/Sep/2022:15:57:06.200 +0000] instanceName="pingdirectory-0-us-east-2" threadID=-1 category=EXTENSIONS severity=NOTICE msgID=1880555611 msg="Administrative alert type=server-started id=43b0bdd1-0439-4ad4-8d2b-4e627daca442 class=com.unboundid.directory.server.core.DirectoryServer msg='The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully'"