SHOULD_BUILD = 'true'
LIBS_CHANGED = ''
def current_repo_name = scm.getUserRemoteConfigs()[0].getUrl().tokenize('/').last().split("\\.")[0]
def scmUrl = scm.getUserRemoteConfigs()[0].getUrl()
pipeline {
    agent any
    parameters {
        //paramaters require for pipeline -Dmetadataversion possiblly defiend here
        string(defaultValue: "7.3_34", description: 'version of metadata', name: 'version')
    }
    stages {
        stage('Setup') {
//             environment {
// //                 GIT_CREDENTIALS = credentials('git-user-credentials-with-token')
//             }

            steps {
                script {
//                     echo "GIT_BRANCH: >>${GIT_BRANCH}<<"
                    prefix = "${GIT_BRANCH}"
                    prefix = prefix.replace("/", "-").replace("origin-", "")
                    echo " ################################################################## GIT_BRANCH:${GIT_BRANCH} prefix:${prefix} current_repo_name:${current_repo_name} BUILD_NUMBER:${BUILD_NUMBER} "
                    echo "QQQQQQQQQQQQQQ scmUrl ${scmUrl}"
                }

                dir
                //         sh './scripts/build.sh --build-number ${BUILD_NUMBER} setup'
                //         sh '''
                //         curl - H "Authorization: Bearer $GIT_CREDENTIALS_PSW" - H "Content-Type: application/json" - s[https: //$%7bSTASH_URL%7d/projects/SAN/repos/automation/raw/SANscreen/Tools/pr-default-tasks.sh?at=refs%2Fheads%2Fmaster]https://${STASH_URL}/projects/SAN/repos/automation/raw/SANscreen/Tools/pr-default-tasks.sh?at=refs%2Fheads%2Fmaster -o /tmp/pr-default-tasks.sh
                //         chmod +x /tmp/pr-default-tasks.sh
                //         '''
                //         sh "/tmp/pr-default-tasks.sh --branch $BRANCH_NAME --repo-name $current_repo_name --git-user $GIT_CREDENTIALS_USR --git-password $GIT_CREDENTIALS_PSW --default-task-description 'Merge latest master and run aut_dev by setting run_integration to y in your dev build'"
            }
        }
    }
//     post {
//         always {
//             //cleanup some stuff
//         }
//     }
}
