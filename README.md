# zssss

import UIKit


class ViewController: UIViewController {


    @IBOutlet weak var Player1: UITextField!

    

    @IBOutlet weak var Player2: UITextField!

    

    @IBOutlet weak var Player1Score: UILabel!

    

    @IBOutlet weak var PlayerScore2: UILabel!

    

    

    @IBOutlet weak var WinnerLabel: UILabel!

    @IBOutlet weak var GameTitle: UILabel!

    override func viewDidLoad() {

       

        super.viewDidLoad()

        // Do any additional setup after loading the view.

    }


    @IBAction func RollADiceButton(_ sender: Any) {

        let score1 = String(arc4random_uniform(6) + 1)

        let score2 = String(arc4random_uniform(6) + 1)

        Player1Score.text = Player1.text!+" roll is: "+score1

        

        PlayerScore2.text = Player2.text!+" roll is: "+score2

        

        if(score1 == score2){

            

            WinnerLabel.text = "The Game is Tie"

        }else{

            if (score1 > score2) {

                

                WinnerLabel.text = Player1.text! + " Won the Game"

                

            }else{

                WinnerLabel.text = Player2.text! + " Won the Game"

            }

            

        }

        

        

    }

    

}
