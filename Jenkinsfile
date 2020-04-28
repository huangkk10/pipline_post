pipeline
{
   agent any

   stages 
   {
      stage('build') 
      {
         steps 
         {
            echo 'build stage'
         }
         post
         {
            always
            {
               echo "stage post always"
            }
         }
      }
   }

   post
   {
      changed
      {
         echo "pipesline post changed"
      }
      always
      {
         echo "pipeline post always"
      }
      success
      {
         echo "pipeline post success"
         mail to: 'huangkk10@gmail.com' subject: "The pipeline success."
      }
   }
}
