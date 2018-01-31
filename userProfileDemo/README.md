# User Profile Demo

Update your database rules engine to only allow authenticated users to read/write to the database AND access their data in the database.




[Manage Users](https://firebase.google.com/docs/auth/web/manage-users)

[Firebase Security](https://firebase.google.com/docs/database/security/)

##Example of firebase rules policy

<pre><code>
{
  "rules":{ 
  	"users": {
      "$uid": {
        ".write": "$uid === auth.uid",
        ".read": "$uid === auth.uid"
      }
    }
  }
}
</code></pre>