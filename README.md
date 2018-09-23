/*
# Swift-4-Xcode-10.0-Projects
Monty Hall Problem solution in swift 4 and Xcode 10.0

Updated solution to Monty Hall Problem (https://en.wikipedia.org/wiki/Monty_Hall_problem) from Swift Algorithm Club (https://github.com/raywenderlich/swift-algorithm-club). The loop I inserted will show how the changed option had more probability.

Ex: Question: If you have 3 options to choose in a show and one of them had a prize. you choose one and then the host reveal one option out of three (which doesn't have a prize and which not chosen by you). Now host gives an option to change your mind/choice. Will you change your mind?

Solution: So the probability of winning the prize based on your original choice is 33.3% and the probability of wining the prize based on the changed choice is 67%. This can be witnessed by simple program with a loop.

*/

//: Playground - noun: a place where people can play
//test this project in playground and increse the loop to see the change

import UIKit
import Darwin

var winOptionSelected = 0
var winOptionChanged = 0
    
/*
var DisclosedChoice = -1
var changeMind = -1
    
    repeat {
        DisclosedChoice = Int(arc4random_uniform(3))
    } while DisclosedChoice == prizeOption || DisclosedChoice == choosenOption
    
    repeat {
        changeMind = Int(arc4random_uniform(3))
    } while changeMind == DisclosedChoice || changeMind == choosenOption
*/

for i in 0...99{
    
    let prizeOption = Int(arc4random_uniform(3))
    let choosenOption = Int(arc4random_uniform(3))
    if choosenOption == prizeOption {
    winOptionSelected += 1
      //check here how many times original choice wins
    } else {
        winOptionChanged += 1
       //check here how many times changed option wins
    }
}
print("In given number of moves \(winOptionSelected) times you win if you stick to your option.")
print("In given number of moves \(winOptionChanged) times you win if you change your mind in second chance.")


//hope this will help you... please comment if you have any questions.
