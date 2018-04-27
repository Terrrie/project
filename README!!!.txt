Here are some brief instructions on how to change the code in order to have
2 different versions of the app to use GitHub's Version Control features:

1. In the 'MainActivity.java' file, open the code and add the following code
after the line that says " /****** Handle new password somehow *******/ "

try{
            String name="", new_pw="";

            Intent intent = getIntent();
            Bundle extras = intent.getExtras();
            if(extras != null){
                name = extras.getString("username");
                new_pw = extras.getString("password");

                for( int i=0; i<users.size(); i++){
                    String[] user = users.get(i);
                    if( user[0].contains( name ) ){
                        user[1] = new_pw;
                    }
                }
            }
        } catch (Exception e){}

2.  In the 'ForgotActivity.java' file, open the code and add the following code
after the line that says " /****** Change user password to new password *******/ "

intent.putExtra("username", name);
intent.putExtra("password", new_password);

===================================================================================

For further information, contact me at tuhafeniheita013@gmail.com

