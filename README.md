# AWS
Implementing AWS SNS and SES Services using Java 

Before Using the Code install AWS CLI in your windows / Linux Machine

Setup Aws Cli
-----------------
  1. Install Python, Don't forget the clink on "Add to path" checkbox during initial stages of python installation
     then use the commands below
      
    pip3 install awscli
    pip3 install --user --upgrade awscli

  2. now create an IAM user with SNS full access. Generate & download it's access keys 
  3. Now use the below command to input the access key and secret key, ( remember the profile_name )
      
      aws configure --profile profile_name 
      region where sns is supported, then return type ( json, txt ... ) 
      
  4. Now this code shd work 


  5. There are 3 Classes in the Project : 

     a . AmazonSESOne
     b . AmazonSESTwo 
     c . AmazonSns

Amazon SES is purely used for SES and to send emails, 
- AmazonSESOne uses SMTP to send messages, the SES STMP keys can be generated in the SES section of AWS 
- AmazonSESTwo uses you credentials configured to send the messages
- AmazonSns uses  "ProfileCredentialsProvider("profile_name")" to fetch the configured Access and Secret Key from the CLI, The Phone    
    number and region can be configured in the code.


Notes
--------------
- Kindly please refer the AWS CLI document while setting up 
- I used the AmazonSns Code for sending OTP Messages to phones. So you've to change the phone number in the code and the region. 
- I also used a one-time password (HOTP and TOTP) library by jchambers for Unique OTP Generation. which can be found here 
  https://github.com/jchambers/java-otp


References - 

1. https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html
