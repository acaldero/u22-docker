# Ubuntu 22.04 LTS in Docker (v2.0)

## Using u22-docker

<html>
 <table>
  <tr>
  <th>Summary</th>
  <th>Example of work session</th>
  </tr>
  <tr>
  <td>
</html>

  * First time + "each time u22-dockerfile is updated":
    * ./u22.sh build

  * To start **3** containers:
    *  ./u22.sh start **3**

  * To get into container **2**:
    *  ./u22.sh bash **2**

  * Being within **2**, to exit:
    *  exit

  * To stop the containers:
    *  ./u22.sh stop

  * Available options for debugging:
    *  ./u22.sh status
    *  ./u22.sh network

<html>
  </td>
  <td>
</html>

  * To start:
    * To start a work session with **2** containers, please execute:
      *  ./u22.sh start **2**
    * To check the containers are running please use:
      *  ./u22.sh status
    * To get the containers internal IP address please use:
      *  ./u22.sh network

  * To work with some container:
    * To get into container **1** out of 2 please execute:
      *  ./u22.sh bash **1**
    * <some work inside container **1** at /work directory>
    * To exit from container **1** please use:
      *  exit

  * To stop:
    * To stop the work session please use:
      *  ./u22.sh stop

<html>
  </td>
  </tr>
 </table>
</html>


**Please beware of**:
  * Any modification outside /work will be discarded on container stopping.
  * Please make a backup of your work "frequently".
  * You might need to use "sudo" before ./u22.sh if your user doesn't belong to the docker group (could be solved by using "sudo usermod -aG docker ${USER}")

