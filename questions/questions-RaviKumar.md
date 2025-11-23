
### How do you revert a change from one branch and add it to another?
Scenario: You make an update and commit to the `master` branch. Afterward, you realize that you should've made this 
change to another branch named `staging`. What do you do? 

#### Assumptions
- The commit has **not** been pushed to the remote repository.
- The response instructions is for the **GitHub Desktop GUI Method**
  
#### Reverting Changes from ``master`` to ``staging``
To move a commit from ``master`` to ``staging``, you must **cherry-pick the commit**.

#### Prerequisite
Ensure that the ``staging`` branch already exists.
(See, *Creating a Branch* for more details.)

#### Cherry-Picking a Commit
Follow these steps in GitHub Desktop:
1. Open the **Current Branch** dropdown
2. Select the ``master`` branch
3. Open the **History** tab
4. Select the commit you want to cherry-pick
5. Right-click the commit and choose:

   ``Cherry-pick commit… → Staging → Cherry-pick <number of commits> to Staging``

#### Reverting Wrong Commit from Master
1. Open the **Current Branch** dropdown
2. Select the ``master`` branch
3. Open the **History** tab
4. Select the commit you want to revert
5. Right-click and choose ``Undo commit…``

### How do you squash git commits?
Scenario: You have a GitHub branch with 5 separate commits. What is the command line sequence to squash those 5 commits 
into a single commit?

The command line sequence ```git rebase -i HEAD~5``` allows you to squash last 5 separate commits into a single commit.

### What is wrong with this sample JSON syntax?

```
{
  "first_name" : "Franz",
  "last_name" : "Kafka",
  "location" : "San Francisco"
  "streams" : true,
  "kafka" : 2.3 
}
```
I observe a syntax error in the JSON syntax sample provided. In the line item "location": "San Francisco", a punctuation comma is missing. The correct JSON syntax is:

```
{
  "first_name": "Franz",
  "last_name": "Kafka",
  "location": "San Francisco",
  "streams": true,
  "kafka": 2.3
}

```

### What is the Kafka broker port?

Scenario: Complete step 1 of [this Confluent Platform quick start](https://docs.confluent.io/platform/current/get-started/platform-quickstart.html) to 
install a local version of Confluent Platform. After completing step 1, what port number is the broker running on?

The Kafka broker port is 9092 on the image confluentinc/cp-server:8.1.0

### What are the default topics created when you install Confluent Platform using the quick start?

Scenario: After you complete step 1 of [this quick start](https://docs.confluent.io/platform/current/get-started/platform-quickstart.html), 
open Control Center at http://localhost:9021/. What are the names of the default topics that are created by Kafka?

After completing step 1 of quick start guide, the following default topics are available in the control center:
-	_internal_confluent_only_broker_info
-	default_ksql_processing_log
-	docker-connect-configs
-	docker-connect-offsets
-	docker-connect-status

### What is the name of the Connect cluster that is created?

Scenario: Complete step 2 of [this quick start](https://docs.confluent.io/platform/current/get-started/platform-quickstart.html). 
What is the name of the Connect cluster that is created?

The name of the connect cluster created is **connect-default**.
