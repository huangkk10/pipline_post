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

            retry(5)
            {
               sh "echo retry"
            }

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
      }
   }
}
