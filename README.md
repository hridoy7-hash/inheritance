# inheritance

<?php
class userData{
    public $user;
    public $userId;

    public function __construct($userName,$userId){
        $this->user=$userName;
        $this->userId=$userId;
      }
      public function display(){
          echo "This username is $this->user and user id is $this->userId ";
      }
}


class Admin extends userData{
    public $level;
    public function display(){
        echo "This username is $this->user and user id is $this->userId and user level is $this->level";
    }

}

$user="Hridoy Hossen";
$id= "171059042";
$object= new userData($user,$id);
$object->display();
//-------------------------------
$user="Admin";
$id= "3424244";
$admin= new Admin($user,$id);
$admin->level="Administrator";
$admin->display();




?>
