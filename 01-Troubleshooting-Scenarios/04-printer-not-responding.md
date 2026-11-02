# Scenario 4: Printer not responding

Level: Basic
Note: Practice scenario. The details are fictional.

## Problem
A user sends a document to the office printer, but nothing prints. The printer shows an error code on its screen.

## Symptoms
- The print job stays in the queue as "Printing" or "Error"
- The printer screen shows an error code
- Other users can't print either

## Diagnostic steps
1. Ask for the exact error code on the printer screen and write it down.
2. Check the basics: power, paper, toner, and paper jams (open all trays and covers).
3. Power cycle the printer. Turn it off, wait 10 seconds, turn it on.
4. Check the printer is on the network. Look at the printer screen for its Wi-Fi or cable connection and its IP address.
5. Ping the printer's IP address from a laptop. It replies, so the network connection is fine.
6. On the user's laptop, open the print queue and look for a stuck job.

## Root cause
A large print job was stuck in the queue and blocked every job behind it.

## Solution
1. Cancel the stuck job in the print queue (if it won't cancel, restart the Print Spooler service)
2. Send a one-page test print
3. Ask the user to print their document again and confirm it works

## Prevention
- Teach users not to send the same job again and again when it seems slow, because that fills the queue
- Give the printer a fixed IP address so computers can always find it

## What I learned
Check the basics first: power, paper, and a stuck queue. Most printer problems are simple.
