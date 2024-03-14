---
title: MT-SMS 
description: A site for learning X from Y
---

# Welcome To Learn X  **From**  Y


This SIMILAR to the site from a learning site for the [Learn X in Y](https://learnxinyminutes.com/) 



>[!tip] The Big Idea:
> ### Learn NEW (PHP) language by references OLD (Python) language
> (EBI) Equivalence-Based Instruction
> Example: Animals  (dog, cat,bird)
> #### What Are The Same ? 
> 
> They both have four legs.
> 
> They cannot fly.
>
> #### What Are Different ? 
> Only a bird has two legs and can fly


  

## TODO's (2h - 2.5h MAX) 
>[!example] TODO's 
> #### How To Learn A Language Fast !
> 
> #### Learn Basic PHP
> 
> #### Learn PHP Required For MainTech Work
>
> #### Implement Ticket (SMS) : First As CLI
>
> #### Integrate Into MainTech
> 
>  *[[Agenda| Full Agenda >> ]]*



.

## Ticket Summary (It LOOKS Complex It's Not)
>[!faq] Ticket Summary (Lots of examples and practices)
> #### Create a fallback  SMS solutions for MainTech
> **Why:** Current Service Provider ClickATell is unreliable
>
> **What:** 
> * Add Twilio as fallback solution if the Primary Service Provider delivery fails.
> * Add feature to define a Primary & Secondary SMS Provider
>
> **Acceptance Criteria:** 
> * Should be config based .env file, who is the PRIMARY and who is the SECONDARY Provider .
> * Make use of Basic OOP Inheritance to define an AbstractSMS BaseClass 
> * Implement Concrete Child Class for each provider
> * Create SMSManager class that decides when to use which
> * As a 'client' of the class you only want to know about SMSManager and it's and to call send.
> * The Concrete Child Classes  SMSClickATell and SMSTwilio will deal with the details of HOW



