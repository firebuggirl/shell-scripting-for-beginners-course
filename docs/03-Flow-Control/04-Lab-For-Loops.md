# Lab For Loop

  - Take me to the [Lab](https://kodekloud.com/courses/1029419/lectures/21506303)


  1. Run this command for the solution

     <details>

     ```
     for mission in lunar-mission mars-mission jupiter-mission saturn-mission mercury-mission
     do
        bash /home/bob/create-and-launch-rocket $mission
     done
     ```
     </details>

  2. Run this command for the solution

     <details>

     ```
     for mission_name in $(cat /tmp/assets/mission-names.txt)
     do
         bash /home/bob/create-and-launch-rocket $mission_name
     done
     ```
     </details>

  3. Run this command for the solution

     <details>

     ```
     for i in {31..40}
     do
             echo $i
     done

     ```
     </details>

  4. Run this command for the solution

     <details>

     ```
     echo -e " Log name   \t      GET      \t      POST    \t   DELETE "
     echo -e "------------------------------------------------------------"
     
     for app in $(cat /tmp/assets/apps.txt)
     do
       get_requests=$(cat /var/log/apps/${app}_app.log | grep "GET" | wc -l)
       post_requests=$(cat /var/log/apps/${app}_app.log | grep "POST" | wc -l)
       delete_requests=$(cat /var/log/apps/${app}_app.log | grep "DELETE" | wc -l)
       echo -e " ${app}    \t ${get_requests}    \t    ${post_requests}   \t   ${delete_requests}"
     
     done
     ```
     </details>

  5. Run this command for the solution

     <details>

     ```
     for file in $(ls images)
     do
             if [[ $file = *.jpeg ]]
                     then
                     new_name=$(echo $file| sed 's/jpeg/jpg/g')
                     mv images/$file images/$new_name
             fi
     done
     ```
     </details>