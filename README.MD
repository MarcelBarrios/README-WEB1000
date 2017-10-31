Quiz 2

Instructions: create a new repository called ng-ds-test. Within this repo, create a README.md file. Copy and paste all of these questions into this README file and answer them.

1.Name and describe the two main operations of a stack (to add and remove data).

  Answer:  To add data we use Push because we want to put it at the end, and to remove data we use Pop because we want to remove the last element from an array and return that element.

2.Name and describe the two main operations of a queue (to add and remove data).

  Answer: We use Enqueue to add an item at the tail, and to remove the item at the head we use Dequeue.

3.Draw the tree resulting from adding the following sequence of numbers to an empty tree: 30, 45, 15, 10, 50, 40, 20, 27

  Answer:        --------------30----------------
                ------15----------------45-------
                --10------20---------40----50----
                -------------27
4.Is this tree balanced? If not, which rotation needs to be done? (Use the following rotation as an example: rightRotation(30), or leftRotation(10))

Answer: It is balanced.

5.Now add 29. Is the tree balanced? If not, which rotation needs to be done? (Use the following rotation as an example: rightRotation(30), or leftRotation(10))
Answer:
             --------------30----------------
             ------15----------------45-------
             --10------20---------40----50----
             -------------27------------------
             ----------------29---------------

  Answer: It is not balanced, and It needs leftRotation(27);

6.Consider the following tree:
------5
---2-----8
-1--3

Now add 0 to the tree. Which one is the first node to go out of balance?
Answer:     ------5
            ---2-----8
            -1--3

      the first node that goes out of balance is 5.

7.How do you fix this node? (Use the following rotation as an example: rightRotation(30), or leftRotation(10))

Answer: rightRotation(2)

8.What are the four main steps of mergesort?
Answer: Divide, Conquer, Combine, Return.

9.Say you have a program which handles the login queue to a game server. The game server is able to log in one person every one second. Assume that one second must elapse after a person logs in with an empty queue before they are removed from the queue. Draw the state of the queue at 12:00:06, considering the following sequence of events:

At 12:00:00 Hades logs in
At 12:00:00 Ares logs in
At 12:00:00 Zeus logs in
At 12:00:00 Buzz Light Year logs in
At 12:00:02 Kanye West logs in
At 12:00:03 Taylor Swift logs in
At 12:00:03 Darkwing Duck logs in
At 12:00:04 Evil Mickey logs in.

Answer:
At 12:00:03 Darkwing Duck logs in
At 12:00:04 Evil Mickey logs in.

10.Solve https://www.hackerrank.com/challenges/compare-the-triplets - be mindful that you are required to print the output to the console in exactly the format that was asked. You are not required to return a value, just print to the console. Also be mindful to use JavaScript.



11.Solve https://www.hackerrank.com/challenges/mini-max-sum - be mindful that you are required to print the output to the console in exactly the format that was asked. You are not required to return a value, just print to the console. Also be mindful to use JavaScript.

process.stdin.resume();
process.stdin.setEncoding("ascii");

let _input = "";
process.stdin.on("data", input => _input += input);
process.stdin.on("end", () => dataP(_input));



const dataP = input => {
   const numbers = input.split(" ").map(i => parseInt(i));
   numbers.sort((a, b) => a - b)
   let minSum = 0;
   let maxSum = 0;
   for(let i = 0; i < numbers.length - 1; i++) {
       minSum += numbers[i];
       maxSum += numbers[i + 1];
   }
   console.log(minSum + " " + maxSum);
};
