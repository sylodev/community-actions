You can use this action to retrieve a leaderboard for anything. Atlas will do the work for you by sorting all the data, displaying it correctly, handling all the errors (if any), making the buttons and more!. 

HOW TO SETUP THE ACTION
1) Import the action into your server
2) To add a user to the leaderboard, you must use the two variables assigned to it. `data` storage variable must be used primarily for all the donations. Atlas scans for all the donations on this first. If you manage to hit the limit, you can use the secondary variable `gdata`

The format to add a user is displayed below

FORMAT_1	-	You can use this in an eval cmd or a slash command to make it easier to add

{=data;{store.get;data}}
{=info.userid;USER_ID}
{=info.dono;DONATION_AMOUNT} // The donation amount means the points/dono to be assigned to the user!
{push;{$data};{$info}}

FORMAT_2	- 	In the form of how Atlas views them
{[  {{"userid":"USER_ID",
      "dono":"DONATION_AMOUNT"}},
    {{"userid2":"USER_ID",
      "dono":"DONATION_AMOUNT"}}, ... ]}

3) After that simply save the storage and watch the lb!
