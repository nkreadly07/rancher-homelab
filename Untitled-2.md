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
#           STARTED: Tue Sep 13 15:41:42 UTC 2022
#          HOST_NAME: pingdirectory-2
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

    ###################################################################################
    #
    #                      PD_STATE: UPDATE
    #                      RUN_PLAN: RESTART
    #

    ###################################################################################
    #            ORCHESTRATION_TYPE: KUBERNETES
    #                      HOST_NAME: pingdirectory-2
    #                    serverUUID: ba181457-7665-3ea9-ac03-5e5a9d61101b
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
    #                 instance name: pingdirectory-2.pingdirectory
    #                      hostname: pingdirectory-2.pingdirectory
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
                         HOST_NAME : pingdirectory-2 
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
          Hostname: pingdirectory-2
           Started: Tue Sep 13 15:41:46 UTC 2022
    ################################################################################
    
    Server Profile pingdirectory
      - Creates an initial PingDirectory with users
      - Prepared for connections from DataSync, DirectoryProxy and DataGovernance
    
    
    ################################################################################


----- Starting hook: /opt/staging/hooks/20-restart-sequence.sh.pre

----- Starting hook: /opt/staging/hooks/10-download-artifact.sh
10-download-artifact.sh: 2022-09-13 15:41:46 INFO export config settings
10-download-artifact.sh: 2022-09-13 15:41:46 INFO MULTI_CLUSTER - false
10-download-artifact.sh: 2022-09-13 15:41:46 INFO PRIMARY_CLUSTER - true
10-download-artifact.sh: 2022-09-13 15:41:46 INFO PD_HTTPS_PORT - 1443
10-download-artifact.sh: 2022-09-13 15:41:46 INFO PD_LDAP_PORT - 1389
10-download-artifact.sh: 2022-09-13 15:41:46 INFO PD_LDAPS_PORT - 1636
10-download-artifact.sh: 2022-09-13 15:41:46 INFO PD_REPL_PORT - 8989
10-download-artifact.sh: 2022-09-13 15:41:46 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
10-download-artifact.sh: 2022-09-13 15:41:46 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
10-download-artifact.sh: 2022-09-13 15:41:46 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
10-download-artifact.sh: 2022-09-13 15:41:46 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
10-download-artifact.sh: 2022-09-13 15:41:46 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
10-download-artifact.sh: 2022-09-13 15:41:46 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
10-download-artifact.sh: 2022-09-13 15:41:46 INFO Private Repo : s3://bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7
10-download-artifact.sh: 2022-09-13 15:41:46 INFO Public Repo  : https://ping-artifacts.s3-us-west-2.amazonaws.com
10-download-artifact.sh: 2022-09-13 15:41:46 INFO [
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
10-download-artifact.sh: 2022-09-13 15:41:46 INFO Download Artifact from https://ping-artifacts.s3-us-west-2.amazonaws.com/pingdirectory/pingdata-extensions/1.0.2
10-download-artifact.sh: 2022-09-13 15:41:47 INFO Artifact successfully downloaded.
10-download-artifact.sh: 2022-09-13 15:41:47 INFO Validating downloaded artifact file
10-download-artifact.sh: 2022-09-13 15:41:47 INFO Download Artifact from s3://bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7/pingdirectory/session-revocation/1.0.1
10-download-artifact.sh: 2022-09-13 15:41:47 INFO Copying: 'pd-session-revocation-1.0.1.zip' to '/opt/staging/pd.profile/server-sdk-extensions'
2022/09/13 15:41:47 Downloading file: s3://bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7/pingdirectory/session-revocation/1.0.1/pd-session-revocation-1.0.1.zip 
2022/09/13 15:41:47 Bucket: bootstrap-customer-hub-astfinanc-pingbinarybucket-k80jqs0xctk7 File: pingdirectory/session-revocation/1.0.1/pd-session-revocation-1.0.1.zip
2022/09/13 15:41:47 Using AWS_REGION: us-east-2
2022/09/13 15:41:47 Concurrency: 0 PartSize: 0
2022/09/13 15:41:47 File: pd-session-revocation-1.0.1.zip  Size: 9331451 bytes
2022/09/13 15:41:47 Successfully downloaded file: /opt/staging/pd.profile/server-sdk-extensions/pd-session-revocation-1.0.1.zip
10-download-artifact.sh: 2022-09-13 15:41:47 INFO Validating downloaded artifact file
pd-session-revocation-1.0.1.zip pingdata-extensions-1.0.2.zip

----- Starting hook: /opt/staging/hooks/20-restart-sequence.sh
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO export config settings
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO MULTI_CLUSTER - false
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO PRIMARY_CLUSTER - true
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO PD_HTTPS_PORT - 1443
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO PD_LDAP_PORT - 1389
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO PD_LDAPS_PORT - 1636
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO PD_REPL_PORT - 8989
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO restarting container
20-restart-sequence.sh: 2022-09-13 15:41:47 INFO Re-generating java.properties for current JVM

The operation was successful.  The Directory Server commands will use the java
arguments and java home specified in the properties file located in
/opt/out/instance/config/java.properties
20-restart-sequence.sh: 2022-09-13 15:41:51 INFO restart-sequence: updating server profile



20-restart-sequence.sh: 2022-09-13 15:41:51 INFO Copying the license key into the PD profiles directory
20-restart-sequence.sh: 2022-09-13 15:41:51 INFO Using /usr/local/secrets/encryption-settings.pin as the encryption-setting.pin file
20-restart-sequence.sh: 2022-09-13 15:41:51 INFO Merging changes from new server profile
Validating source and existing servers ..... Done
Exporting the encryption settings definitions to temporary file
/tmp/encryption-settings-export-15486420389090212554.tmp

Preparing existing server ..... Done
Setting up the server with the new profile ..... Done
Importing the encryption settings definitions from temporary file
/tmp/encryption-settings-export-15486420389090212554.tmp
Skipping export and re-import since the "--reimportData never" argument was
specified

Merging in configuration and data from the existing server ..... Done
Merging in topology and license configuration from the existing server ..... Done
Setting the inter-server certificate ..... Done
Validating server ..... Done
Cleaning up after replace ..... Done
20-restart-sequence.sh: 2022-09-13 15:44:02 INFO manage-profile replace-profile status: 0
20-restart-sequence.sh: 2022-09-13 15:44:02 INFO Copy beluga profile files after restart

----- Starting hook: /opt/staging/hooks/07-apply-server-profile.sh
merging /opt/staging/instance to /opt/out/instance

20-restart-sequence.sh: 2022-09-13 15:44:10 INFO Not rebuilding indexes as there are no indexes to rebuild with status NEW or UNTRUSTED
20-restart-sequence.sh: 2022-09-13 15:44:10 INFO updating tools.properties

----- Starting hook: /opt/staging/hooks/185-apply-tools-properties.sh
Configuring tools.properties

20-restart-sequence.sh: 2022-09-13 15:44:10 INFO updating encryption settings

----- Starting hook: /opt/staging/hooks/15-encryption-settings.sh
15-encryption-settings.sh: 2022-09-13 15:44:10 INFO export config settings
15-encryption-settings.sh: 2022-09-13 15:44:10 INFO MULTI_CLUSTER - false
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO PRIMARY_CLUSTER - true
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO PD_HTTPS_PORT - 1443
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO PD_LDAP_PORT - 1389
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO PD_LDAPS_PORT - 1636
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO PD_REPL_PORT - 8989
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO encryption-settings: starting processing of encryption-settings definitions
15-encryption-settings.sh: 2022-09-13 15:44:11 INFO encryption-settings: creating a new encryption definition
15-encryption-settings.sh: 2022-09-13 15:44:16 INFO encryption-settings: Unable to add the new encryption settings definition for use in the server:
Encryption settings definition
E6FCD9B397C6B66C6BCC55E623FB50C1B46C15C145A7CD08C9E53D0E60249274 already
exists in the database (id=1879310781 EncryptionSettingsDB.java:999
8.3.0.0-20210617212340.000Z-29a2bc05).
15-encryption-settings.sh: 2022-09-13 15:44:16 INFO encryption-settings: finished processing all encryption-settings definitions

20-restart-sequence.sh: 2022-09-13 15:44:16 INFO enabling the replication sub-system in offline mode
20-restart-sequence.sh: 2022-09-13 15:44:16 INFO configuring userRoot for base DN dc=amstock,dc=com

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
20-restart-sequence.sh: 2022-09-13 15:44:29 INFO configure base DN dc=amstock,dc=com update status: 0
20-restart-sequence.sh: 2022-09-13 15:44:38 INFO Number of sub entries of DN dc=amstock,dc=com in userRoot backend: 44518
20-restart-sequence.sh: 2022-09-13 15:44:38 INFO Replication base DN dc=amstock,dc=com already added
20-restart-sequence.sh: 2022-09-13 15:44:38 INFO add base DN dc=amstock,dc=com status: 0
----- Starting hook: /opt/staging/hooks/185-offline-enable-wrapper.sh
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO export config settings
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO MULTI_CLUSTER - false
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO PRIMARY_CLUSTER - true
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO PD_HTTPS_PORT - 1443
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO PD_LDAP_PORT - 1389
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO PD_LDAPS_PORT - 1636
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO PD_REPL_PORT - 8989
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable-wrapper.sh: 2022-09-13 15:44:38 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable-wrapper.sh: 2022-09-13 15:44:39 INFO Topology descriptor file does not exist or is empty - creating it at /tmp/tmp.BGeBjj
185-offline-enable-wrapper.sh: 2022-09-13 15:44:39 INFO Topology descriptor JSON file '/tmp/tmp.BGeBjj' contents:
{"us-east-2":{"hostname":"pingdirectory.ping-cloud.svc.cluster.local","replicas":3}}
185-offline-enable-wrapper.sh: 2022-09-13 15:44:39 INFO offline enable configuration:
{
  "descriptor_json"     : "/tmp/tmp.BGeBjj",
  "inst_root"           : "/opt/out/instance",
  "hostname_prefix"     : "pingdirectory",
  "local_tenant_domain" : "astfinancial.us1.ping.cloud",
  "local_region"        : "us-east-2",
  "local_num_replicas"  : 3,
  "local_ordinal"       : 2,
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
185-offline-enable.sh: 2022-09-13 15:44:39 INFO export config settings
185-offline-enable.sh: 2022-09-13 15:44:39 INFO MULTI_CLUSTER - false
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PRIMARY_CLUSTER - true
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_HTTPS_PORT - 1443
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_LDAP_PORT - 1389
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_LDAPS_PORT - 1636
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_REPL_PORT - 8989
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:44:39 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:44:39 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
185-offline-enable.sh: 2022-09-13 15:44:39 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:44:39 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:44:39 INFO export config settings
185-offline-enable.sh: 2022-09-13 15:44:39 INFO MULTI_CLUSTER - false
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PRIMARY_CLUSTER - true
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_HTTPS_PORT - 1443
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_LDAP_PORT - 1389
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_LDAPS_PORT - 1636
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_REPL_PORT - 8989
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:44:39 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:44:39 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:44:39 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
185-offline-enable.sh: 2022-09-13 15:44:39 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:44:39 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:44:39 INFO Begin for '/opt/out/instance'
Processing completed.  Transformed 707 entries.
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Difference between /opt/out/instance/config/config.ldif and /tmp/185-offline-enable.sh.XXXXcMFOcd/config.ldif.nowrap
--- /opt/out/instance/config/config.ldif
+++ /tmp/185-offline-enable.sh.XXXXcMFOcd/config.ldif.nowrap
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
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Validate the descriptor.json syntax
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Verifying descriptor.json content
{"us-east-2":{"hostname":"pingdirectory.ping-cloud.svc.cluster.local","replicas":3}}
185-offline-enable.sh: 2022-09-13 15:44:43 INFO local_region: us-east-2
185-offline-enable.sh: 2022-09-13 15:44:43 INFO local_hostname: pingdirectory.ping-cloud.svc.cluster.local
185-offline-enable.sh: 2022-09-13 15:44:43 INFO local_count: 3
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Deleting server groups: replication-servers all-servers
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Removing all existing server instances
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Creating top level server instance DN 'cn=Server Instances,cn=Topology,cn=config'
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Replacing local server instance name to 'cn=Server Instances,cn=Topology,cn=config'
185-offline-enable.sh: 2022-09-13 15:44:43 INFO Updating existing replication entries for replication server DN 'cn=replication server,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config'
185-offline-enable.sh: 2022-09-13 15:44:43 INFO removing DNs no longer being replicated
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Updating existing replication domain o=platformconfig.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Updating existing replication domain o=appintegrations.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Updating existing replication domain dc=amstock,dc=com.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Modifications being applied from /tmp/185-offline-enable.sh.XXXXcMFOcd/mods.ldif LDIF file:
dn: cn=replication-servers,cn=Server Groups,cn=Topology,cn=config
changeType: delete

dn: cn=all-servers,cn=Server Groups,cn=Topology,cn=config
changeType: delete

dn: cn=82b6d867-0e43-44dc-972b-b2a90327ea4b,cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=3eecd4cf-859d-4874-9d6d-028cc27d2a2d,cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config
changeType: delete

dn: cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config
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
createTimestamp: 20220913154439.879Z

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
createTimestamp: 20220913154439.879Z
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
createTimestamp: 20220913154439.879Z
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
createTimestamp: 20220913154439.879Z
ds-cfg-replication-domain-server-id: 1201
ds-cfg-replication-domain-server-id: 1203
ds-cfg-replication-domain-server-id: 1205


dn: cn=config
changeType: modify
replace: ds-cfg-instance-name
ds-cfg-instance-name: pingdirectory-2-us-east-2


dn: cn=replication server,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-replication-server-id
ds-cfg-replication-server-id: 1200
-
replace: ds-cfg-replication-port
ds-cfg-replication-port: 8989


dn: cn=o_platformconfig,cn=domains,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-server-id
ds-cfg-server-id: 1201
-
replace: cn
cn: o_platformconfig
-
replace: ds-cfg-base-dn
ds-cfg-base-dn: o=platformconfig

dn: cn=o_appintegrations,cn=domains,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-server-id
ds-cfg-server-id: 1203
-
replace: cn
cn: o_appintegrations
-
replace: ds-cfg-base-dn
ds-cfg-base-dn: o=appintegrations

dn: cn=dc_amstock_dc_com,cn=domains,cn=Multimaster Synchronization,cn=Synchronization Providers,cn=config
changeType: modify
replace: ds-cfg-server-id
ds-cfg-server-id: 1205
-
replace: cn
cn: dc_amstock_dc_com
-
replace: ds-cfg-base-dn
ds-cfg-base-dn: dc=amstock,dc=com
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Calling ldifmodify for mods '/tmp/185-offline-enable.sh.XXXXcMFOcd/mods.ldif'
Successfully completed processing.  Source entries read:  707.  Entries
updated:  19.  Entries not updated:  688.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO There are no zero (unused) ports in /opt/out/instance/config/config.ldif.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Admin user 'admin' already exists.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO group 'replication-servers' does not already exist - creating
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Creating 'replication-servers' group with members:  pingdirectory-0-us-east-2 pingdirectory-1-us-east-2 pingdirectory-2-us-east-2.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO group 'all-servers' does not already exist - creating
185-offline-enable.sh: 2022-09-13 15:44:44 INFO Creating 'all-servers' group with members:  pingdirectory-0-us-east-2 pingdirectory-1-us-east-2 pingdirectory-2-us-east-2.
185-offline-enable.sh: 2022-09-13 15:44:44 INFO applying dsconfig from file /tmp/185-offline-enable.sh.XXXXcMFOcd/batch.dsconfig:
dsconfig create-server-group \
  --group-name "replication-servers" \
   --set member:pingdirectory-0-us-east-2 --set member:pingdirectory-1-us-east-2 --set member:pingdirectory-2-us-east-2

dsconfig create-server-group \
  --group-name "all-servers" \
   --set member:pingdirectory-0-us-east-2 --set member:pingdirectory-1-us-east-2 --set member:pingdirectory-2-us-east-2

[13/Sep/2022:15:44:47 +0000] SEVERE_WARNING The Directory Server has sent an alert notification generated by class com.unboundid.directory.server.extensions.ConfigFileHandler (alert type offline-config-change-detected, alert ID 424f9487-1019-4847-95b7-b035f09537dc):  The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913154346Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=all-servers,cn=Server Groups,cn=topology,cn=config', 'cn=replication-servers,cn=Server Groups,cn=topology,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=3eecd4cf-859d-4874-9d6d-028cc27d2a2d,cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=82b6d867-0e43-44dc-972b-b2a90327ea4b,cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config'
[13/Sep/2022:15:44:51 +0000] SEVERE_WARNING The Directory Server has sent an alert notification generated by class com.unboundid.directory.server.extensions.ConfigFileHandler (alert type offline-config-change-detected, alert ID c6ef0e86-bfb2-4021-b164-9fbe66bf3faf):  The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913154346Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=all-servers,cn=Server Groups,cn=topology,cn=config', 'cn=replication-servers,cn=Server Groups,cn=topology,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=3eecd4cf-859d-4874-9d6d-028cc27d2a2d,cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=82b6d867-0e43-44dc-972b-b2a90327ea4b,cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config'

Arguments from tool properties file:  --useSSL  --hostname localhost --port
1636 --bindDN cn=administrator --bindPasswordFile
/usr/local/secrets/root-user-password --trustAll

Batch file '/tmp/185-offline-enable.sh.XXXXcMFOcd/batch.dsconfig' contains 2 commands.

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

185-offline-enable.sh: 2022-09-13 15:44:58 INFO restoring the original header
185-offline-enable.sh: 2022-09-13 15:44:58 INFO End for '/opt/out/instance'
185-offline-enable-wrapper.sh: 2022-09-13 15:44:58 INFO offline enable complete
20-restart-sequence.sh: 2022-09-13 15:44:58 INFO offline replication enable status: 0
20-restart-sequence.sh: 2022-09-13 15:44:58 INFO restart sequence done


----- Starting hook: /opt/staging/hooks/50-before-post-start.sh


Starting server in foreground: (/opt/out/instance/bin/start-server --nodetach)
----- Starting hook: /opt/staging/hooks/80-post-start.sh
80-post-start.sh: 2022-09-13 15:44:58 INFO export config settings
80-post-start.sh: 2022-09-13 15:44:58 INFO MULTI_CLUSTER - false
80-post-start.sh: 2022-09-13 15:44:58 INFO PRIMARY_CLUSTER - true
80-post-start.sh: 2022-09-13 15:44:58 INFO PD_HTTPS_PORT - 1443
80-post-start.sh: 2022-09-13 15:44:58 INFO PD_LDAP_PORT - 1389
80-post-start.sh: 2022-09-13 15:44:58 INFO PD_LDAPS_PORT - 1636
80-post-start.sh: 2022-09-13 15:44:58 INFO PD_REPL_PORT - 8989
80-post-start.sh: 2022-09-13 15:44:58 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
80-post-start.sh: 2022-09-13 15:44:58 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
80-post-start.sh: 2022-09-13 15:44:58 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
80-post-start.sh: 2022-09-13 15:44:58 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
80-post-start.sh: 2022-09-13 15:44:58 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
80-post-start.sh: 2022-09-13 15:44:58 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
80-post-start.sh: 2022-09-13 15:44:58 INFO starting post-start hook
80-post-start.sh: 2022-09-13 15:44:58 INFO running ldapsearch test on this container (pingdirectory-2)
Sleeping 3 seconds (max: 15)...
2022-09-13T15:45:04,316+0000 [17 1] com.newrelic INFO: New Relic Agent: Loading configuration file "/opt/shared-dir/newrelic.yml"
2022-09-13T15:45:04,429+0000 [17 1] com.newrelic INFO: Using default collector host: collector.newrelic.com
2022-09-13T15:45:04,553+0000 [17 1] com.newrelic INFO: New Relic Agent: Writing to log file: /opt/staging/logs/newrelic_agent.log
Sleeping 9 seconds (max: 15)...
WARNING: An illegal reflective access operation has occurred
WARNING: Illegal reflective access by com.newrelic.weave.weavepackage.NewClassAppender (file:/opt/staging/newrelic.jar) to method java.net.URLClassLoader.addURL(java.net.URL)
WARNING: Please consider reporting this to the maintainers of com.newrelic.weave.weavepackage.NewClassAppender
WARNING: Use --illegal-access=warn to enable warnings of further illegal reflective access operations
WARNING: All illegal access operations will be denied in a future release



********************************************************************************
[13/Sep/2022:15:45:10.746 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=de72fcb1-31e2-42df-bbc2-438a51907fc4 class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913154346Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=3eecd4cf-859d-4874-9d6d-028cc27d2a2d,cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=82b6d867-0e43-44dc-972b-b2a90327ea4b,cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



[13/Sep/2022:15:45:12.346 +0000] category=CORE severity=NOTICE msgID=458886 msg="Ping Identity Directory Server 8.3.0.0 (build 20210618165156Z, Rv8.3.0.0-GA) starting up"



********************************************************************************
[13/Sep/2022:15:45:13.612 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3277462 msg="Schema configuration file 50-AST-DIT.ldif in directory /opt/out/instance/config/schema contains more than one entry.  Only the first entry will be examined, and the additional entries will be ignored"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:13.612 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3277462 msg="Schema configuration file 52-AdminGroups.ldif in directory /opt/out/instance/config/schema contains more than one entry.  Only the first entry will be examined, and the additional entries will be ignored"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:13.619 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276992 msg="Schema configuration file 53-AST-ACI.ldif in directory /opt/out/instance/config/schema cannot be parsed because an unexpected error occurred while trying to read its contents as an LDIF entry:  Unable to parse LDIF entry starting at line 1 because the line '-' does not include an attribute name (id=5439494 LDIFReader.java:2007 8.3.0.0-20210617212340.000Z-29a2bc05)"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:13.620 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3277462 msg="Schema configuration file 54-AST-Dev-Test-Users_20210920.ldif in directory /opt/out/instance/config/schema contains more than one entry.  Only the first entry will be examined, and the additional entries will be ignored"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:13.620 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276992 msg="Schema configuration file 61-RemovePermissiveACI.ldif in directory /opt/out/instance/config/schema cannot be parsed because an unexpected error occurred while trying to read its contents as an LDIF entry:  Unable to parse LDIF entry starting at line 2 because the line '-' does not include an attribute name (id=5439494 LDIFReader.java:2007 8.3.0.0-20210617212340.000Z-29a2bc05)"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:13.621 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276992 msg="Schema configuration file 62-ModPwdState.ldif in directory /opt/out/instance/config/schema cannot be parsed because an unexpected error occurred while trying to read its contents as an LDIF entry:  Unable to parse LDIF entry starting at line 1 because the line '-' does not include an attribute name (id=5439494 LDIFReader.java:2007 8.3.0.0-20210617212340.000Z-29a2bc05)"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:13.668 +0000] category=CONFIG severity=SEVERE_WARNING msgID=3276995 msg="An objectclass read from schema configuration file 98-ast.ldif conflicts with another objectclass already read into the schema:  Unable to register object class 'astUser' with the server schema because its OID 'astuser-oid' conflicts with the OID of an existing object class 'astUser'.  The later objectclass definition will be used"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:13.801 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=40a9e0b4-5b47-479f-ab38-c1f246dca59c class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913154346Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=3eecd4cf-859d-4874-9d6d-028cc27d2a2d,cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=82b6d867-0e43-44dc-972b-b2a90327ea4b,cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



[13/Sep/2022:15:45:14.235 +0000] category=CORE severity=NOTICE msgID=1879508001 msg="The third-party extension class com.pingidentity.pingcloud.pingdatasdk.pingdirectory.P14CPassThroughPreParsePlugin, version 1.0.2, has been loaded into the server using the configuration defined in cn=PingOne for Customers Pass-Through Authentication Pre-Parse Plugin,cn=Plugins,cn=config"
Sleeping 12 seconds (max: 15)...



********************************************************************************
[13/Sep/2022:15:45:17.466 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=de72fcb1-31e2-42df-bbc2-438a51907fc4 class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913154346Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=3eecd4cf-859d-4874-9d6d-028cc27d2a2d,cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=82b6d867-0e43-44dc-972b-b2a90327ea4b,cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:17.467 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=offline-config-change-detected id=40a9e0b4-5b47-479f-ab38-c1f246dca59c class=com.unboundid.directory.server.extensions.ConfigFileHandler msg='The server has detected that configuration file '/opt/out/instance/config/config.ldif' was altered with the server offline and differs from the latest configuration archive file '/opt/out/instance/config/archived-configs/config-20220913154346Z.gz'.  This may indicate that dsconfig was used in offline mode, the server was updated, or that the configuration file was manually edited.  The entries which differ between the current and archived configuration include:  'ds-cfg-backend-id=userRoot,cn=Backends,cn=config', 'cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-0-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-1-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=3eecd4cf-859d-4874-9d6d-028cc27d2a2d,cn=Cipher Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config', 'cn=82b6d867-0e43-44dc-972b-b2a90327ea4b,cn=MAC Secret Keys,cn=pingdirectory-2-us-east-2,cn=Server Instances,cn=Topology,cn=config''"
********************************************************************************



[13/Sep/2022:15:45:17.472 +0000] category=EXTENSIONS severity=NOTICE msgID=1880555611 msg="Administrative alert type=server-starting id=c8033ce8-3b71-483b-bb82-d0d73eb6be9b class=com.unboundid.directory.server.core.DirectoryServer msg='The Directory Server is starting'"



********************************************************************************
[13/Sep/2022:15:45:18.564 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=je-environment-not-closed-cleanly id=7960f9b8-a141-41e0-8081-165f3753eb10 class=com.unboundid.directory.server.backends.jeb.RootContainer msg='The server has detected that the Berkeley DB JE environment located in directory '/opt/out/instance/db/appintegrations' may not have been closed cleanly the last time it was opened (or that the backend has just been restored from a backup taken with the server online).  The database environment may need to replay changes from the end of the transaction log to guarantee the integrity of the data, and in some cases this may take a significant amount of time to complete'"
********************************************************************************



[13/Sep/2022:15:45:19.927 +0000] category=JEB severity=NOTICE msgID=1887895580 msg="Starting cache priming for 44 databases in backend appintegrations"
[13/Sep/2022:15:45:19.951 +0000] category=JEB severity=NOTICE msgID=1887896003 msg="Preloaded 32 entry records and 250 index records (97% embedded within internal database structure) in 0 seconds"
[13/Sep/2022:15:45:19.954 +0000] category=JEB severity=NOTICE msgID=1887895587 msg="The database cache now holds 7MB of data and is 1 percent full"



********************************************************************************
[13/Sep/2022:15:45:20.091 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=je-environment-not-closed-cleanly id=965fc3a2-a853-426a-a3de-2a07ed8cb3c3 class=com.unboundid.directory.server.backends.changelog.ChangelogBackend msg='The server has detected that the Berkeley DB JE environment located in directory '/opt/out/instance/db/changelog' may not have been closed cleanly the last time it was opened (or that the backend has just been restored from a backup taken with the server online).  The database environment may need to replay changes from the end of the transaction log to guarantee the integrity of the data, and in some cases this may take a significant amount of time to complete'"
********************************************************************************



[13/Sep/2022:15:45:20.290 +0000] category=CONFIG severity=NOTICE msgID=1882652783 msg="Initializing mirrored topology and cluster-wide configuration"



********************************************************************************
[13/Sep/2022:15:45:20.920 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=je-environment-not-closed-cleanly id=438df4e2-a5fb-45ed-9464-14db1f989902 class=com.unboundid.directory.server.backends.jeb.RootContainer msg='The server has detected that the Berkeley DB JE environment located in directory '/opt/out/instance/db/platformconfig' may not have been closed cleanly the last time it was opened (or that the backend has just been restored from a backup taken with the server online).  The database environment may need to replay changes from the end of the transaction log to guarantee the integrity of the data, and in some cases this may take a significant amount of time to complete'"
********************************************************************************



[13/Sep/2022:15:45:21.260 +0000] category=JEB severity=NOTICE msgID=1887895580 msg="Starting cache priming for 23 databases in backend platformconfig"
[13/Sep/2022:15:45:21.267 +0000] category=JEB severity=NOTICE msgID=1887896003 msg="Preloaded 41 entry records and 1315 index records (95% embedded within internal database structure) in 0 seconds"
[13/Sep/2022:15:45:21.268 +0000] category=JEB severity=NOTICE msgID=1887895587 msg="The database cache now holds 3MB of data and is 2 percent full"



********************************************************************************
[13/Sep/2022:15:45:21.499 +0000] category=CONFIG severity=SEVERE_WARNING msgID=1882325089 msg="Backend 'userRoot' is configured with multiple base DNs.  While this is currently supported, this capability should be considered deprecated and may be removed in the future.  Configuring a backend with multiple base DNs may introduce complexity in replication (where some features like online initialization via binary copy may not be available) or other areas and is not recommended.  This warning may be disabled via the warn-for-multiple-base-dns global configuration property, but it is strongly recommended that you first contact Ping Identity support to discuss the use of multiple base DNs in your directory environment"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:21.536 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=je-environment-not-closed-cleanly id=964640d4-2c06-4163-b228-c0bc2f1d7191 class=com.unboundid.directory.server.backends.jeb.RootContainer msg='The server has detected that the Berkeley DB JE environment located in directory '/opt/out/instance/db/userRoot' may not have been closed cleanly the last time it was opened (or that the backend has just been restored from a backup taken with the server online).  The database environment may need to replay changes from the end of the transaction log to guarantee the integrity of the data, and in some cases this may take a significant amount of time to complete'"
********************************************************************************



Sleeping 14 seconds (max: 15)...
[13/Sep/2022:15:45:29.751 +0000] category=CORE severity=NOTICE msgID=1879507304 msg="Invoking an explicit garbage collection because backend initialization took longer than 12185 milliseconds, which is greater than the forced-gc-prime-duration of 10000 milliseconds (maxMemory=3221225472, allocatedMemory=3221225472, usedMemory=284436056, freeMemory=2936789416)"
[13/Sep/2022:15:45:29.954 +0000] category=CORE severity=NOTICE msgID=1879507305 msg="Explicit garbage collection completed after 203 milliseconds (maxMemory=3221225472, allocatedMemory=3221225472, usedMemory=284436056, freeMemory=3015003592)"



********************************************************************************
[13/Sep/2022:15:45:29.985 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=debug-logging-enabled id=15eb8a66-f1d2-45a3-ba59-7104584380e2 class=com.unboundid.directory.server.loggers.debug.TextDebugLogPublisher msg='A Debug Log Publisher is enabled. When Debug Targets are configured to restrict what is logged, the performance impact is typically negligible. However, it is good practice to disable the Debug Log Publisher once the required information has been collected'"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:29.990 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=no-enabled-alert-handlers id=8beba0ba-0ed8-424d-998c-bffe474c7b83 class=com.unboundid.directory.server.core.AlertHandlerConfigManager msg='No alert handlers have been enabled. Alerts will be written to logs/errors, but administrators will not be otherwise notified of current or impending problems. The server uses alerts to self-report many problems or precursors to potential problems. If an administrator does not receive these alerts, then there might be a server outage that was avoidable. In production environments, we strongly recommend enabling the SMTP Alert Handler to send emails, the JMX or SNMP Alert Handler to send notifications to a monitoring application, or creating a custom alert handler. In non-product environments, this alarm can be suppressed by adding 'no-enabled-alert-handlers' to the 'suppressed-alarm' configuration property on the Alarm Manager configuration object'"
********************************************************************************



[13/Sep/2022:15:45:31.058 +0000] category=PROTOCOL severity=NOTICE msgID=1881604184 msg="HTTP Connection Handler HTTPS Connection Handler using 8 threads"
[13/Sep/2022:15:45:35.796 +0000] category=CORE severity=NOTICE msgID=1879508001 msg="The third-party extension class com.pingidentity.ps.pd.plugin.ast.SessionRevocationAccountStatusNotificationHandler, version 1.0.1, has been loaded into the server using the configuration defined in cn=Session Revocation Notification Handler,cn=Account Status Notification Handlers,cn=config"
[13/Sep/2022:15:45:36.256 +0000] category=EXTENSIONS severity=NOTICE msgID=1880556375 msg="Successfully set the delegated admin ACI"



********************************************************************************
[13/Sep/2022:15:45:36.275 +0000] category=EXTENSIONS severity=SEVERE_ERROR msgID=1880359005 msg="Administrative alert type=delegated-admin-configuration-errors id=95255a80-2619-4c47-9760-18e670ba47a3 class=com.unboundid.directory.server.extensions.dadmin.DelegatedAdminAlertGenerator msg='The Delegated Admin configuration has the following errors: Delegated Admin Rights 'administrator-user-dadmin' Admin User DN 'uid=admin,dc=amstock,dc=com' references a nonexistent entry'"
********************************************************************************



********************************************************************************
[13/Sep/2022:15:45:37.179 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=je-environment-not-closed-cleanly id=7466e5d9-d301-42eb-ba85-6956c50874ae class=com.unboundid.directory.server.replication.server.ReplicationServer msg='The server has detected that the Berkeley DB JE environment located in directory '/opt/out/instance/changelogDb' may not have been closed cleanly the last time it was opened (or that the backend has just been restored from a backup taken with the server online).  The database environment may need to replay changes from the end of the transaction log to guarantee the integrity of the data, and in some cases this may take a significant amount of time to complete'"
********************************************************************************



[13/Sep/2022:15:45:42.439 +0000] category=REPLICATION severity=NOTICE msgID=118947974 msg="The replication server startup min replication backlog count is 5000"
[13/Sep/2022:15:45:42.448 +0000] category=REPLICATION severity=NOTICE msgID=118947923 msg="Replication server startup min replication backlog processing completed. All local replicas available when the server was started have reported below the configured threshold of 5000"
dn: cn=config

80-post-start.sh: 2022-09-13 15:45:45 INFO pod ordinal: 2; multi-cluster: false
80-post-start.sh: 2022-09-13 15:45:45 INFO resetting password for user DN: uid=administrator,ou=admins,o=platformconfig



********************************************************************************
[13/Sep/2022:15:45:45.118 +0000] category=EXTENSIONS severity=SEVERE_WARNING msgID=1880228292 msg="The Linux kernel parameter vm.swappiness is set to '60' instead of '0'.  This non-zero setting allows Linux to swap temporarily inactive parts of the JVM out of memory to disk.  When the JVM later accesses large amounts of this swapped out memory (for instance during a garbage collection cycle), the server can experience pauses of several seconds where no processing occurs.  We strongly recommend setting this value to '0' by executing 'sysctl -w vm.swappiness=0' as root to change the current value in the operating system and by adding a line 'vm.swappiness = 0' to /etc/sysctl.conf to ensure that the correct setting is applied when the system restarts. If a system performance service such as tuned is used, also apply the vm.swappiness setting to the active profile or disable the service. To check for an active performance profile run the tuned-adm active command"
********************************************************************************



[13/Sep/2022:15:45:45.147 +0000] category=CORE severity=NOTICE msgID=1879507495 msg="One or more third-party extensions have been loaded into the server.  The DNs of the configuration entries for the third-party extensions are:  'cn=Session Revocation Notification Handler,cn=Account Status Notification Handlers,cn=config', 'cn=PingOne for Customers Pass-Through Authentication Pre-Parse Plugin,cn=Plugins,cn=config'"
[13/Sep/2022:15:45:45.147 +0000] category=CORE severity=NOTICE msgID=458887 msg="The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully"
[13/Sep/2022:15:45:45.147 +0000] category=EXTENSIONS severity=NOTICE msgID=1880555611 msg="Administrative alert type=server-started id=ae42a4d1-ae42-457c-9a7c-30e988033bad class=com.unboundid.directory.server.core.DirectoryServer msg='The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully'"

# Password Modify Extended Result:
# Result Code:  53 (unwilling to perform)
# Diagnostic Message:  The provided new password cannot be the same as the
#      current password or any password in the password history

The password modify extended operation failed with result code 53 (unwilling to
perform) and diagnostic message The provided new password cannot be the same as
the current password or any password in the password history
80-post-start.sh: 2022-09-13 15:45:47 INFO password reset for DN uid=administrator,ou=admins,o=platformconfig status: 53
80-post-start.sh: 2022-09-13 15:45:47 INFO resetting password for user DN: uid=pingfederate,ou=devopsaccount,o=platformconfig

# Password Modify Extended Result:
# Result Code:  53 (unwilling to perform)
# Diagnostic Message:  The provided new password cannot be the same as the
#      current password or any password in the password history

The password modify extended operation failed with result code 53 (unwilling to
perform) and diagnostic message The provided new password cannot be the same as
the current password or any password in the password history
80-post-start.sh: 2022-09-13 15:45:50 INFO password reset for DN uid=pingfederate,ou=devopsaccount,o=platformconfig status: 53
80-post-start.sh: 2022-09-13 15:45:50 INFO resetting password for user DN: cn=admin

# Password Modify Extended Result:
# Result Code:  53 (unwilling to perform)
# Diagnostic Message:  The provided new password cannot be the same as the
#      current password or any password in the password history

The password modify extended operation failed with result code 53 (unwilling to
perform) and diagnostic message The provided new password cannot be the same as
the current password or any password in the password history
80-post-start.sh: 2022-09-13 15:45:52 INFO password reset for DN cn=admin status: 53
80-post-start.sh: 2022-09-13 15:45:52 INFO not initializing replication data because INITIALIZE_REPLICATION_DATA is false
80-post-start.sh: 2022-09-13 15:45:52 INFO post-start complete

----- Starting hook: /opt/staging/hooks/100-tail-logs.sh
100-tail-logs.sh: 2022-09-13 15:45:52 INFO export config settings
100-tail-logs.sh: 2022-09-13 15:45:52 INFO MULTI_CLUSTER - false
100-tail-logs.sh: 2022-09-13 15:45:52 INFO PRIMARY_CLUSTER - true
100-tail-logs.sh: 2022-09-13 15:45:52 INFO PD_HTTPS_PORT - 1443
100-tail-logs.sh: 2022-09-13 15:45:52 INFO PD_LDAP_PORT - 1389
100-tail-logs.sh: 2022-09-13 15:45:52 INFO PD_LDAPS_PORT - 1636
100-tail-logs.sh: 2022-09-13 15:45:52 INFO PD_REPL_PORT - 8989
100-tail-logs.sh: 2022-09-13 15:45:52 INFO PD_CLUSTER_DOMAIN_NAME - pingdirectory.ping-cloud.svc.cluster.local
100-tail-logs.sh: 2022-09-13 15:45:52 INFO PD_SEED_LDAP_HOST - pingdirectory-0.pingdirectory.ping-cloud.svc.cluster.local
100-tail-logs.sh: 2022-09-13 15:45:52 INFO LOCAL_HOST_NAME - pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local
100-tail-logs.sh: 2022-09-13 15:45:52 INFO LOCAL_INSTANCE_NAME - pingdirectory-2-us-east-2
100-tail-logs.sh: 2022-09-13 15:45:52 INFO DNS_TO_ENABLE - o=platformconfig o=appintegrations dc=amstock,dc=com
100-tail-logs.sh: 2022-09-13 15:45:52 INFO UNINITIALIZED_DNS - o=platformconfig o=appintegrations dc=amstock,dc=com
100-tail-logs.sh: 2022-09-13 15:45:52 INFO Tailing logs: /opt/out/instance/logs/access /opt/out/instance/logs/change-notifications.log /opt/out/instance/logs/errors /opt/out/instance/logs/failed-ops /opt/out/instance/logs/expensive-write-ops /opt/out/instance/logs/replication


/opt/out/instance/logs/expensive-write-ops # Logger initialized at 12/Sep/2022:21:54:01 +0000
/opt/out/instance/logs/expensive-write-ops [12/Sep/2022:21:56:04 +0000] MODIFY RESULT threadID=401 conn=-4 op=29224 msgID=29225 dn="ds-cfg-backend-id=userRoot,cn=Backends,cn=config" resultCode=0 etime=1577.660 mostExpensivePhase="INVOKING_BACKEND_PROCESSING" mostExpensivePhaseTimeMicros=1576830.348 mostExpensiveAggregatePhase="INVOKING_BACKEND_PROCESSING" mostExpensiveAggregatePhaseTimeMicros=1576830.348 phaseTimesMicros="INVOKING_BACKEND_PROCESSING=1576830.348"
/opt/out/instance/logs/expensive-write-ops # Logger initialized at 13/Sep/2022:15:43:51 +0000
/opt/out/instance/logs/expensive-write-ops # Logger shut down at 13/Sep/2022:15:44:01 +0000
/opt/out/instance/logs/expensive-write-ops # Logger initialized at 13/Sep/2022:15:45:17 +0000
/opt/out/instance/logs/errors [13/Sep/2022:15:45:37.179 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=EXTENSIONS severity=SEVERE_WARNING msgID=1880227932 msg="Administrative alert type=je-environment-not-closed-cleanly id=7466e5d9-d301-42eb-ba85-6956c50874ae class=com.unboundid.directory.server.replication.server.ReplicationServer msg='The server has detected that the Berkeley DB JE environment located in directory '/opt/out/instance/changelogDb' may not have been closed cleanly the last time it was opened (or that the backend has just been restored from a backup taken with the server online).  The database environment may need to replay changes from the end of the transaction log to guarantee the integrity of the data, and in some cases this may take a significant amount of time to complete'"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:42.144 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=15138878 msg="Connected to server pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local:8989 for dc=amstock,dc=com [id: 1200]"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:42.347 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=15138878 msg="Connected to server pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local:8989 for o=appintegrations [id: 1200]"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:42.389 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=15138878 msg="Connected to server pingdirectory-2.pingdirectory.ping-cloud.svc.cluster.local:8989 for o=platformconfig [id: 1200]"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:42.439 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=118947974 msg="The replication server startup min replication backlog count is 5000"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:42.448 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=REPLICATION severity=NOTICE msgID=118947923 msg="Replication server startup min replication backlog processing completed. All local replicas available when the server was started have reported below the configured threshold of 5000"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:45.118 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=EXTENSIONS severity=SEVERE_WARNING msgID=1880228292 msg="The Linux kernel parameter vm.swappiness is set to '60' instead of '0'.  This non-zero setting allows Linux to swap temporarily inactive parts of the JVM out of memory to disk.  When the JVM later accesses large amounts of this swapped out memory (for instance during a garbage collection cycle), the server can experience pauses of several seconds where no processing occurs.  We strongly recommend setting this value to '0' by executing 'sysctl -w vm.swappiness=0' as root to change the current value in the operating system and by adding a line 'vm.swappiness = 0' to /etc/sysctl.conf to ensure that the correct setting is applied when the system restarts. If a system performance service such as tuned is used, also apply the vm.swappiness setting to the active profile or disable the service. To check for an active performance profile run the tuned-adm active command"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:45.147 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=CORE severity=NOTICE msgID=1879507495 msg="One or more third-party extensions have been loaded into the server.  The DNs of the configuration entries for the third-party extensions are:  'cn=Session Revocation Notification Handler,cn=Account Status Notification Handlers,cn=config', 'cn=PingOne for Customers Pass-Through Authentication Pre-Parse Plugin,cn=Plugins,cn=config'"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:45.147 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=CORE severity=NOTICE msgID=458887 msg="The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully"
/opt/out/instance/logs/errors [13/Sep/2022:15:45:45.148 +0000] instanceName="pingdirectory-2-us-east-2" threadID=-1 category=EXTENSIONS severity=NOTICE msgID=1880555611 msg="Administrative alert type=server-started id=ae42a4d1-ae42-457c-9a7c-30e988033bad class=com.unboundid.directory.server.core.DirectoryServer msg='The Directory Server (Ping Identity Directory Server 8.3.0.0 build 20210618165156Z, Rv8.3.0.0-GA) has started successfully'"