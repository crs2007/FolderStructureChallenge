# Case Study: Folder Structure Mapping Challenge
This case was taken as an out of scope (oos) training for internal challenge.

## General Rules:
This task is going to be our playground.
The task will be divided into two parts, which could affect one on the other. 
But, as in the real world you will only see the 2nd part after you will finish the 1st part.

Please, set a meeting with me to have a grooming upon the request to see that all is understood by you.
The task is individual and not a group task.

### Part One – Key part working Solo…:
On this part I will be the product owner, I well know the business requirements for this product. feel free to ask me anything that is not clear or covered.
You will be a DBA responsible for design, performance and DB implementation.
Please, note any assumption you will take for others, to understand your implementation.

You are owner of event monitoring system.
The system tables are:
- FOLDER- a table of folders that contains the Folder ID and the ID of its direct parent - Folder (Id, PerantId, Path).
- USER– a table of users in the system. User (UserId, Name).
- EVENT- for tracking who did what on the system. Event (EventId, Date, OparationCode, FolderId, Userid).

For ex. Yesterday user1 have an action of “OpenFolder” on C:\Temp.
Other, user2 did an oparation of “CloseFolder” on C:\Users.

More information:
- Usually there are 1 million events per day. 
- The system has about 10K users.
- Max depth of folders is 50.  For ex. C:\a\b\c\d\...50.
- Keep in mind, the service\agent will run on more than one computer. but this will make the challange to a path I wish to ignore for now.

The system should run on a root path to collect all the folder mapping into a table, while keeping hierarchy of folder Id and the parent Id
Please, **plan a design** of the system, with the proper types, connections and indexes.

Based on UI request for – 
- How many event per user?
	- Write a query and show the plan.
- How many events a user have based on a specific root folder (and it sub folders) on a specific day
	- Write a query and show the plan.

### Solution ground rules:
- The script could be runnable on any given time without errors - rerunnable script.
- Choose any server you want(not prod, obviously) - create a new database.
- Create a dedicated SQL user for this service - Please, provide the connection string - Server, Database, User & Passward.
- All script should be within **one** sql file.
- The script should have a cleanup for all of our mess.

#### Bonus Point
- The solution sould be provided with dockerfile\dockercompose of SQL Server with the lateset version.

### Part Two- Key part shared task for Dev & DBA:
[Part 2](https://github.com/crs2007/FolderStructureChallenge/Part2.md)

### Disclaimer
This code and information are provided "AS IS" without warranty of any kind, either expressed or implied, including but not limited to the implied warranties or merchantability and/or fitness for a particular purpose.  

### Warranty
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### License
This script is free to download and use for personal, educational, and internal corporate purposes, provided that this header is preserved. 
Redistribution or sale of this script, in whole or in part, is prohibited without the author's express written consent.
