# sirajganj
Ratan Sing
Create a new repository
A repository contains all project files, including the revision history. Already have a project repository elsewhere? Import a repository.

Owner
/
Repository name
Great repository names are short and memorable. Need inspiration? How about fuzzy-barnacle?

Description (optional)
Public
Anyone on the internet can see this repository. You choose who can commit.
Private
You choose who can see and commit to this repository.
Initialize this repository with:
Skip this step if you’re importing an existing repository.

Add a README file
This is where you can write a long description for your project. Learn more.
Add .gitignore
Choose which files not to track from a list of templates. Learn more.
Choose a license
A license tells others what they can and can't do with your code. Learn more.
You are creating a public repository in your personal account.
Permission in manifest
<uses-permission android:name="android.permission.CALL_PHONE"></uses-permission>
Execute a phone call
Intent intent = new Intent(Intent.ACTION_CALL);
intent.setData(Uri.parse("tel:+436641234567"));
startActivity(intent);
Call a contact
Intent intent = new Intent(Intent.ACTION_CALL);
intent.setData(Uri.parse("content://contacts/people/"+contact_id));
startActivity(intent);
Display the dialer with a number
Intent intent = new Intent(Intent.ACTION_DIAL);
intent.setData(Uri.parse("tel:+436641234567"));
startActivity(intent);
Listen to incoming/outgoing phone calls
Permission in manifest file
<uses-permission android:name="android.permission.READ_PHONE_STATE">
   </uses-permission>
Extend the phone state listener
class MyPhoneStateListener extends PhoneStateListener{
          public void onCallStateChanged(int state, String incomingNumber){
                   super.onCallStateChanged(state, incomingNumber);
                   switch (state){
                             case TelephonyManager.CALL_STATE_IDLE:
                                      //phone in idle state
                                      break;
                             case TelephonyManager.CALL_STATE_OFFHOOK:
                                      //phone in offhook state
                                      break;
                             case TelephonyManager.CALL_STATE_RINGING:
                                      //phone is ringing
                                      break;
                             default:
                                      break;
                   }
          }
}
Register the listener
TelephonyManager mTelephonyMgr = (TelephonyManager)getSystemService(Context.TELEPHONY_SERVICE);
mTelephonyMgr.listen(new MyPhoneStateListener(), PhoneStateListenermedia.LISTEN_CALL_STATE);

 
 
