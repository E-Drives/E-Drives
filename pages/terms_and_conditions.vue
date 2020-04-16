<template>
  <v-container>
    <v-row>
      <v-col>
        <h1 class="secondary--text">Terms and Conditions</h1>
      </v-col>
    </v-row>
    <v-row v-for="(item) in items" :key="item.title">
      <v-col>
        <p>{{ item.title }}</p>
        <v-container fluid>
          <v-row v-for="(subitem) in item.points" :key="subitem.title">
            <v-col>
              <p>{{ subitem.title }}</p>
              <template v-if="subitem.subpoints">
                <v-container container>
                  <v-row v-for="(supersubitem) in subitem.subpoints" :key="supersubitem.title">
                    <v-col>
                      <p>{{ supersubitem.title }}</p>
                      <template v-if="supersubitem.supersubpoints">
                        <v-container fluid>
                          <p
                            v-for="(lastpoint, index) in supersubitem.supersubpoints"
                            :key="index"
                          >{{lastpoint}}</p>
                        </v-container>
                      </template>
                    </v-col>
                  </v-row>
                </v-container>
              </template>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        title: "(1) User",
        points: [
          {
            title:
              "(1.1) The driver of the vehicle shall be considered to be the user and all transactions will be executed solely between the user and E Drives. The following agreement is between the user and E Drives. The agreement governs the terms and conditions of usage of E Drives services such as our website, iOS and android application and rental service."
          },
          {
            title:
              "(1.2) E Drives reserves the right to make any necessary changes in the terms and conditions of the agreement without any prior notice. In the case of any alterations to the agreement, the user will be notified through on the E Drives website or Mobile Application. An email will also be sent to the user."
          },
          {
            title:
              "(1.3) It is considered that a user has read and agreed to the latest terms and conditions at the time of booking the vehicle. A booking is confirmed once the payment has been processed and any such payment is considered an agreement by the respective user to abide by the terms and conditions mentioned herein. In case a user is found to violate any criteria listed in this document, E Drives may revoke his/her membership and/or refuse service without any prior notice."
          }
        ]
      },
      {
        title: "(2) REGISTRATION",
        points: [
          {
            title:
              "(2.1) It is mandatory for every user to register on our website or through our iOS and android application on a mobile device. Users are responsible for providing and maintaining current email, cell phone, address, and other account information at the time of registration. A user will be permitted to book a vehicle only after he/she has obtained a registered account on the E Drives website or mobile application."
          },
          {
            title:
              "(2.2) The user must be minimum 18 years of age and should have a valid driving license issued by the concerned regional transport office. E Drives retains the right to refuse membership to any applicant, even if he/she satisfies the above criteria. Granting of membership is solely on the discretion of E Drives."
          },
          {
            title:
              "(2.3) E Drives vehicles should be driven only by E Drives members. If a person is not registered on E Drives as an active member, he/she will not be allowed to drive the vehicle. By applying for membership, an applicant authorizes E Drives to verify the submitted documents through the concerned authorities."
          },
          {
            title:
              "(2.4) A user is not allowed to create multiple accounts with same driving license. E Drives retains the right to cancel membership and ride if a user is found to be using same driving license for creating multiple accounts."
          }
        ]
      },
      {
        title: "(3) PERSONAL INFORMATION AND DOCUMENTS",
        points: [
          {
            title:
              "(3.1) The user must upload a scanned image or a photograph of his/her license on our website/APP . Only Documents issued by the Government of India such as Original Driver’s license, Aadhaar card, Passport, etc. will be considered as valid ID proof. PAN card or Learner's license will not be accepted as valid government id proof."
          },
          {
            title:
              "(3.2) If a user is unable to verify their identity, the booking shall be considered void. The user must present their Original Driving License to the authorised E Drives Staff at the pickup point. The possession of vehicle will not be granted to a user in case he fails to meet the above requirements."
          },
          {
            title:
              "(3.3) A photograph(s) of the user and the documentation that they provide will be taken at the time of vehicle pick-up, for security purposes. This is to avoid cases of fraud & theft. These photographs will not be shared with any third parties and will only be used for identifying the user under the purview of the trip that they take with E Drives."
          }
        ]
      },
      {
        title: "(4) TERMS OF VEHICLE USE",
        points: [
          {
            title:
              "(4.1) E Drives vehicles are solely for the purpose B2B delivery of goods such as food. The vehicle cannot be used as a taxi or for transporting people. E Drives vehicles cannot be used for races, exhibitions and/or any contests. E Drives vehicles cannot be used for towing, pushing and/or propelling another vehicle or object."
          },
          {
            title:
              "(4.2) E Drives vehicles cannot be used by a person under the influence of (a) Alcohol and/or (b) Any mind altering substance which can impair the user’s ability to drive. Use of narcotic substances is strictly prohibited. If a user is found to be under the influence of these substances, E Drives will not grant possession of the vehicle to the user. The booking fee will be reimbursed to the user’s account as per E Drives’s Refund Policy and the user can be blocked from making any bookings with E Drives. Incase users consume alcohol after the ride has started and gets into any unexpected events the User will be solely responsible for all outcomes thereon (Insurance liability, third party damages, self-damages, police involvements etc)."
          },
          {
            title:
              "(4.3) Users will not be allowed to carry the following items on the vehicle: Weapons or any sharp or inflammable object which may cause damage to the vehicle or endanger human life. Any item/object whose possession has been deemed illegal by the Indian Penal Code. Any item or object which compromises the stability, safety or performance of the vehicle and/or the passengers. E Drives holds the right to refuse a booking if the user is found to possess any of the above items. The vehicle will not be used in a negligent or abusive manner. In the case of non-compliance, appropriate actions may be taken against the user by the concerned authorities."
          },
          {
            title:
              "(4.4) E Drives vehicles can be used only in the Republic of India. Use of the vehicles is subject to the laws of India. The vehicle cannot be driven in areas where entry is prohibited by the central or state government. The user must ensure that the number of passengers in the vehicle does not exceed the seating capacity of the vehicle. In case of non-compliance, the entire sum of security deposit will be retained by E Drives. The vehicle cannot be used for any activity which is deemed illegal by the Indian Penal Code. The terms of vehicle use listed above are non-exhaustive. Any activity judged inappropriate by E Drives in its sole discretion will be deemed as a violation of agreement. Illegal use of the vehicle will be reported to the concerned authorities by E Drives followed by the suspension or termination of service immediately."
          }
        ]
      },
      {
        title: "(5) BOOKINGS",
        points: [
          {
            title:
              "(5.1) All bookings have to be made solely by the registered user themselves via our Website, iOs or Android platforms well in advance and prior to pick up. Bookings are processed by our system automatically on a first come first serve basis. E Drives does not guarantee the availability of any particular vehicle at any given time. Vehicle availability is dynamically updated in our system to reflect real-time changes."
          },
          {
            title:
              "(5.2) In case if any additional charges are to be paid, we strongly recommend to make payment Online via credit/debit card."
          },
          {
            title:
              "(5.3) Extension will be granted if and only if the vehicle is available for the requested period of time. Booking rides extension is not possible within 4 hours of selected end time."
          },
          {
            title:
              "(5.4) An extension to the rental period of the vehicle will be granted subject to availability. The charges for the extension period will be applicable as per normal rates as applicable."
          },
          {
            title:
              "(5.5) All expenses incurred during the rental period on the vehicle such as parking fee, fine, challans etc. will be borne by the user."
          },
          {
            title:
              "(5.6) ‘Charging: Vehicle charging need to be done by the user itself. By plugging the charger to any 5A socket will work , It will take 4-5 hours to completely charge the vehicle."
          }
        ]
      },
      {
        title: "(6) VEHICLE PICK UP AND RETURN",
        points: [
          {
            title:
              "(6.1) The user can collect the pre-booked vehicle from the designated E Drives parking after verifying his/her identity and on completing the requisite paperwork. Booking time is calculated from the moment, the user gains possession of the vehicle’s keys. Prior to taking possession, it is the User's responsibility to inspect the vehicle carefully. In the event of any damages or malfunction, the user should inform E Drives immediately. If a user opts for home-pickup, a charge of Rs.150 will be levied."
          },
          {
            title:
              "(6.2) It is the responsibility of the user to return the vehicle in the same condition as at the time of pickup. In case the interior and/or the exterior of the vehicle is found to be soiled and/or damaged, cleaning charges and/or penalty will apply accordingly subject to a maximum of Rs. 1000 or depending on the extent of the damage, to be decided by E Drives after the ride has ended."
          },
          {
            title:
              "(6.3) E Drives requests its users to kindly check all the features of the vehicle. In the event of any queries, the user is free to contact a E Drives official. In case the user is dissatisfied with the performance of the vehicle, he/she must inform a E Drives official at the time of pickup. In such an event the user will be provided an alternate vehicle of his/her choice as per availability. In case no alternate vehicles are available, the booking deposits will be reimbursed to the user’s bank account or E Drives wallet as per specified by the user at the time of booking."
          },
          {
            title:
              "(6.4) In order to return possession, the user must hand over the keys of the vehicle to a E Drives employee at the designated parking space. If the keys are not returned, E Drives will consider that the user is yet to return possession and the user will be billed accordingly. The vehicle must be returned at the authorized E Drives pickup point only. In case the user fails to return the vehicle on time for any reason whatsoever, penalty charges will apply accordingly."
          },
          {
            title:
              "(6.5) In case of a drop at any satellite location, if the user reaches the drop location before the ride end time, he will have to wait for the E Drives employee to reach the location, for a duration not exceeding 1 hour which will be calculated after the customer has informed the corresponding site of his arrival."
          }
        ]
      },
      {
        title: "(7) SAFETY",
        points: [
          {
            title:
              "(7.1) The Safety of E Drives users and passengers is a top priority. All vehicles are examined periodically in order to ensure that they are in compliance with India’s vehicle safety standards."
          },
          {
            title:
              "(7.2) E Drives expects its users to ensure the following to help us avoid safety issues: (i) The user must ensure that all passengers wear safety belts or helmets. (ii)The number of passengers must not exceed the seating capacity of the vehicle. E Drives reserves the right to fine or block a user due to non-compliance of the above."
          },
          {
            title:
              "(7.3) E Drives is not responsible for any accident and/or injury caused to the driver and/or any of the passengers due to personal negligence or negligence of the driver.If an accident occurs,FIR/NOC will be required from the customer. Additionally, driver's original driving license will be held for insurance claiming purpose, which will be returned after about 30 days depending on the insurance claim formalities."
          }
        ]
      },
      {
        title: "(8) SECURING THE VEHICLE",
        points: [
          {
            title:
              "(8.1) The user is responsible for the security of the vehicle. The user is held liable to ensure that the vehicle is adequately protected from expected adverse weather conditions and is parked in areas taking appropriate precautions to avoid any untoward incidents."
          },
          {
            title:
              "(8.2) In the event of theft, the user must report the incident to E Drives immediately and file a complaint at the nearest police station. The user will be held responsible for any discrepancy or misinformation if any in the filing of the complaint and appropriate action may be taken by the concerned authorities, legal or otherwise."
          },
          {
            title:
              "(8.3) The user must ensure the safety of all equipment in the vehicle which has been provided by E Drives. In case any equipment is misplaced by the user, he/she will be charged for the same at the discretion of E Drives."
          },
          {
            title:
              "(8.4) In case of preventable theft of the GPS device, the user will be charged a penalty as per the discretion of E Drives."
          },
          {
            title:
              "(8.5) The user is responsible for the safety of their belongings. Any item, electronic device or personal belonging left in the vehicle will be returned to the user (if found) after due verification. E Drives however does not guarantee the return of any items left behind."
          }
        ]
      },
      {
        title: "(9) REFUND & REIMBURSEMENT",
        points: [
          {
            title:
              "(9.1) E Drives is not liable to reimburse any expenses borne by a user due to cancellation of any third party associated plans that are not connected with E Drives or the services provided by E Drives; due to any vehicle breakdown, accident, damage or issues caused due to the vehicle or service."
          },
          {
            title:
              "(9.2) The user will be given a refund in the following cases:",
            subpoints: [
              {
                title:
                  "(9.2.a) When a booking is cancelled by the user through the E Drives mobile application or website. Alternatively, the user may also contact the customer care and request a cancellation. After charging our cancellation fees as mentioned below, any remaining amount paid for the booking will be processed to the original method of payment. The refund will be processed within a maximum timeframe of 7-9 working days.",
                supersubpoints: [
                  "In case of cancellations prior to 24 hours of pickup time, user will be charged 5% of the total transaction amount subject to a maximum of Rs.2000.",
                  "For cancellations made within 24 hours of pickup time, user will be charged 15% of the transaction amount subject to a maximum of Rs.2000.",
                  "In case a user fails to show up for his reservation or cancels the ride 2 hours before the pickup time, the booking shall be treated as a No Show and only 60% of the billing amount and security deposit shall be reimbursed(if applicable).",
                  "In case a ride is cancelled due to inability to produce an Original valid license or valid Govt. Id during ride pickup, 15% deductions will be applicable. Any coupon used will not be re-activated in this case.",
                  "If a user with blocked license makes a booking, the ride would be cancelled with 5% deductions."
                ]
              },
              {
                title:
                  "(9.2.b) When a booking is cancelled by us due to unavailability of vehicles:",
                supersubpoints: [
                  "At times when we are unable to provide a vehicle for a booking due to reasons such as accident, damage, service, late handover by previous user etc.; we will process a full refund of the entire amount of the booking back to the original method of payment. The refund will be processed within a maximum timeframe of 7-9 working days."
                ]
              }
            ]
          },
          {
            title:
              "(9.3) The user will be given a reimbursement in the following cases:",
            subpoints: [
              {
                title:
                  "(9.3.a) Minor repairs (expense under Rs.1,000) such as changing bulbs etc."
              },
              {
                title:
                  "(9.3.b) For damages which require expenditure in excess of Rs. 1,000 the user is requested to inform a E Drives official before initiating any repairs. If the user initiates any repairs without informing E Drives, no reimbursement will be given."
              },
              {
                title:
                  "(9.3.c) The user must submit a printed receipt with his/her name written on it. Hand written receipts or receipts without the name of the user will not be entertained. The receipt must be handed over to a E Drives employee while the vehicle is being returned. Late submission of receipts will not be entertained. Receipts will be verified to validate expenses that occurred during the time of the issue or booking."
              },
              {
                title:
                  "(9.3.d) The particulars mentioned herewith are non-exhaustive and E Drives reserves the right to process reimbursement based on due internal investigation and verification of claims."
              }
            ]
          }
        ]
      },
      {
        title: "(10) CLEANLINESS and MAINTENANCE",
        points: [
          {
            title:
              "(10.1) E Drives conducts periodical checks on vehicle performance and ensures that hired vehicles are clean. E Drives expects its users to help us maintain our standards of cleanliness. The user must ensure that the vehicle is not soiled while returning possession."
          },
          {
            title:
              "(10.2) Use of chewing gum, tobacco or any tobacco based product on the vehicle is strictly prohibited. Users will be penalised in case ash, spit marks or remains of chewing gum are detected on the vehicle at the time when possession of the vehicle is returned."
          },
          {
            title:
              "(10.3) Burning of any substance on the vehicle is strictly prohibited. This is not limited to but includes cigarettes, incense sticks or any form of medication/drugs."
          },
          {
            title:
              "(10.4) E Drives reserves the right to block, penalise, fine the user at our own discretion in event of non-compliance of the above."
          }
        ]
      },
      {
        title: "(11) BREAKDOWN OR MEMBER FAILURE",
        points: [
          {
            title:
              "(11.1) In the event of vehicle breakdown or member failure, the user should inform E Drives immediately. In case the vehicle cannot be repaired at the location of breakdown, a replacement vehicle will be provided by E Drives, subject to availability within 10kms radius of E Drives pickup points."
          },
          {
            title:
              "(11.2) The user will have to bear the expenses of towing, repair and other costs if a replacement vehicle is not available or Road Side Assistance(RSA) is unable to resolve the issue or the breakdown id due to customer negligence."
          },
          {
            title:
              "(11.3) For any issues that the user experiences with the vehicle mechanical/electrical condition, we urge the user to bring it to our attention by informing our Customer Contact Centre or our Fleet Executives. Issues that are brought to our attention within 10 kms of the ride start point will be duly noted and hence considered as a valid issue with the vehicle. Issues that are brought to our attention or informed of beyond 10 kms of the ride start point will be considered to have occurred due to negligent, harsh, rash, incorrect use of the vehicle by the user as member failure and will not be entertained. Issues with vehivle components, particularly that of motor, brakes or battery, will be noted only if brought to our attention within 10 kms of the ride start point."
          },
          {
            title:
              "(11.4) This list is non-exhaustive due to the variability in issues caused as part of any vehicle and E Drives reserves the right to deny claims of reimbursement for issues stemming due to member failure as defined above"
          }
        ]
      },
      {
        title: "(12) TRAFFIC RULES VIOLATION AND OTHER INCIDENTS",
        points: [
          {
            title:
              "(12.1) It is the responsibility of the user to inform E Drives in case of any incident which has caused damage to the vehicle and/or any public or private property or any incident which has caused injury to individual(s) and/or animal(s). It is mandatory for the user to file a police report in such an event regardless of liability or fault."
          },
          {
            title:
              "(12.2) In such an event the user must provide the following details to E Drives: Name, address and the license number of the user driving the vehicle at the time of the incident. Name, address and contact number of witnesses (if any). Circumstances of the incident describing the immediate environment of the incident and position of the vehicle prior to the incident. In the event of any lawsuit, users are expected to assist the authorities with investigations (if any). In case any lawsuit against a user is proved in the court of law, E Drives reserves the right to revoke membership of the individual."
          },
          {
            title:
              "(12.3) The user is responsible for traffic rule violations (if any). This includes but is not limited to wrong parking, over speeding, breaking red light at a crossing and toll violations. The user is liable to pay any penalty charges involved. In the event of toll violation, the user is must inform E Drives immediately. If E Drives learns of such an event from a third party, the user will be informed though an e-mail. The user must bear the relevant fine to the concerned authority and submit a proof of compliance to E Drives. In case the user has prior knowledge of such violations, E Drives is not obligated to inform the user. The responsibility of any unreported traffic rule violation rests solely with the user and E Drives will not bear any responsibility whatsoever."
          },
          {
            title:
              "(12.4) In case of any accident/total loss of the vehicle, it is mandatory that the user provides an NOC to E Drives obtained from their local RTO, which issued the user’s license, stating that the user was not involved or associated with any such incidents that occurred previously in any manner and that the user was not involved in any such accidents or has any registered complaint against them for the same."
          }
        ]
      },
      {
        title: "(13) INSURANCE AND LIABILITY",
        points: [
          {
            title:
              "(13.1) Member deductible obligation If a user is in compliance with the Terms and Conditions of the E Drives, the company shall provide primary liability protection, which is the extent of claims / liabilities covered by E Drives’s vehicle insurer, on E Drives vehicles for claims and/or liabilities arising out of the use or operation of the vehicle by the Member. User will be responsible for any associated deductible personally attributable to the user."
          },
          {
            title:
              "(13.2) If it is determined that losses will exceed the user’s coverage as provided by E Drives, the user will be responsible for excess charges E Drives does not take responsibility of theft or damage to the user’s or any third party’s belongings. In case of annulment of the Insurance policy due to user's negligence, rash driving or any such incident, user has to pay the repair cost of the vehicle."
          },
          {
            title:
              "(13.3) Liability protection does not apply bodily injury, death or property damage, other than to the vehicle, arising from the use of E Drives vehicle as permitted by this agreement and applicable law. Such protection excludes any claim made by the user or the user’s immediate family members who live with the member or are travelling with the member at the time of the incident."
          },
          {
            title:
              "(13.4) The user indemnifies and holds E Drives, its parent and affiliates and their respective directors, officers, employees, shareholders, agents, attorneys, assigns and successors-in-interest, harmless for all losses, liabilities, damages, injuries, claims, demands, costs, attorney fees and other expenses incurred by E Drives (A Loss) arising from: The use or possession of a E Drives vehicle by a user. The user’s non-compliance with this agreement."
          },
          {
            title:
              "(13.5) This Agreement is intended for the benefit of Member and E Drives and no other party may claim rights hereunder, whether as a third-party beneficiary or otherwise. Under no circumstances will E Drives be liable to any third party for indirect, incidental, special or consequential damages arising from or related to thisagreement or use of E Drives vehicle and service."
          }
        ]
      },
      {
        title: "(14) LEGAL DISPUTES AND CONFLICTS",
        points: [
          {
            title:
              "(14.1) The courts of Bengaluru, Karnataka, India have the sole and exclusive jurisdiction in the event of any legal dispute or conflict between E Drives and its users arising from the services of E Drives. The user must pay E Drives’s attorney fees and bear the cost of legal proceedings relating to this agreement, including appeals. A user must immediately notify and deliver to E Drives every summons, complaint, document, or notice of any kind received by the user in any way relating to an accident, theft, or other circumstances related to the E Drives vehicle."
          }
        ]
      },
      {
        title: "(15) SEVERABILITY AND INTEGRATED AGREEMENT",
        points: [
          {
            title:
              "(15.1) If any term, provision, covenant or condition of this Agreement is held invalid or unenforceable for any reason, the remainder of the provisions will continue in full force and effect as if this Agreement had been executed with the invalid portion eliminated. The Parties further agree to substitute for the invalid provision a valid provision that most closely approximates the intent and economic effect of the invalid provision. This Agreement, together with the User Guide, Trip Process, member application, Fee Policy / Rate Schedule, and any applicable consent forms, along with any amendments hereto, encompasses the entire agreement between user and E Drives, and supersedes all previous understandings and agreements between the user and E Drives. The user acknowledges and represents that he or she has not relied on any representation, assertion, guarantee, warranty, collateral contract or other assurance, except those set out in this Agreement, made by or on behalf of any other party or any other person or entity whatsoever, prior to the execution of this Agreement."
          }
        ]
      },
      {
        title: "(16) FEE POLICY",
        points: [
          {
            title:
              "(16.1) Conditions Rental charges will apply on an daily basis. Time between 0 to 59 minutes shall be considered by E Drives as a complete hour and the rental charges will be calculated accordingly."
          }
        ]
      },
      {
        title: "(17) TAXES and EXPENSES",
        points: [
          {
            title:
              "(17.1) All charges are inclusive of GST. E Drives retains the rights to change rental rates at any point of time."
          }
        ]
      },
      {
        title: "(18) PENALTY",
        points: [
          {
            title:
              "(18.1) If a customer is found drunk at the time of drop , Rs.1000/- fine will be levied along with the damage cost. Also, the customer will be liable for the complete damage repair cost."
          },
          {
            title:
              "(18.2) Customers are required to drop the vehicle at the drop location chosen at the time of booking. Failing to do so, he will be fined Rs.200/-. Additionally, overtime charges will be fined if another booking coincides with the booking."
          },
          {
            title:
              "(18.3) Smoking is strictly prohibited in and around the vehicle. Penalty of Rs.1000/- fine will be charged,if found guilty."
          },
          {
            title:
              "(18.4) In the case of further delay, Overtime charges would be calculated as Late Hours X Double the Hourly Charges."
          },
          {
            title:
              "(18.5) E Drives shall bear no penalty imposed on the vehicle due to negligent driving on part of the user."
          },
          {
            title:
              "(18.6) Parking challans, if any will have to be borne by the user."
          },
          {
            title:
              "(18.7) In the event of battery, motor or other damage , the customer will be liable to pay for the damage cost (as applicable)."
          },
          {
            title:
              "(18.8) In the event of any traffic rule violation or parking fine, the member must inform E Drives immediately. E Drives may ask for a copy of the challan in such an event."
          },
          {
            title:
              "(18.9) If the user damages or misplaces any attachment or accessory provided with the vehicle, E Drives reserves the right to charge the appropriate amount from the user."
          },
          {
            title:
              "(18.10) If the user has incurred any dues over and above that of the initial booking amount when dropping off the vehicle at the drop off site location and is unable to settle the dues at that time, then the user will have to sign a declaration provided by us promising to settle the dues and leave the original documents of license, government ID, etc. as surety. The documents can be collected by the user from the site location once dues have been settled."
          },
          {
            title:
              "(18.11) In the event of user having any penalties/dues outstanding with E Drives, E Drives reserves the right to charge reminder fees and default interest. E Drives also reserves the right to utilize third parties for the recovery of dues from a user."
          },
          {
            title:
              "(18.12) E Drives reserves the right to prohibit a user from booking any rides until all dues associated with the user account have been paid to E Drives in full."
          },
          {
            title:
              "(18.13) The user would be charged with a penalty in case any accessory such as tools or documents, belonging to E Drives is found missing during the end ride."
          }
        ]
      },
      {
        title: "(19) DISPUTE MANAGEMENT",
        points: [
          {
            title:
              "(19.1) In case of dispute raised by a user, the E Drives confirms if the user has used the service. If the service was not used, we track the payment with our payment partner and a full refund is initiated. If the payment is not captured at our end, we contact the payment partner to process the full refund for the user."
          },
          {
            title:
              "(19.2) E Drives reserves the right to change the terms and conditions mentioned herewith. Notice of such changes will be intimated to the user in a timely manner. Such intimation shall be considered discharged when available and accessible from our E Drives website or mobile application. Such intimation will be provided via email or sms to the most recent email address /mobile numer provided on the User's profile, subsequent to article 1.3."
          }
        ]
      },
      {
        title: "(20) AADHAR E-SIGN",
        points: [
          {
            title:
              "(20.1) By submitting Aadhaar number to E Drives India, you hereby authorize E Drives to collect, encrypt ,store and authenticate your Aadhaar number and demographic details (Information) against UIDAI database by itself or via NSDL e-governance Infra Ltd, an Authentication User Agency duly licensed by UIDAI via Digio.in before updating your account."
          },
          {
            title:
              "(20.2) E Drives will use your aadhar number to verify your identity and to collect e-signs against the SLA documentations."
          },
          {
            title:
              "(20.3) E Drives may use your demographic and biometric/OTP (Or any similar authentication mechanism) information for the purpose of Aadhar based authentication/e-KYC and e-sign."
          },
          {
            title:
              "(20.4) E Drives may share the Aadhaar data with government law enforcement agenrices in case of any legal case/theft etc."
          },
          {
            title:
              "(20.5) E Drives stores your aadhar verified details in encrypted form and in no manner has the access to your real aadhar number. Only you can see your aadhaar number in your profile."
          }
        ]
      },
      {
        title: "(21) ACTIVA/CLIQ BOOKINGS OF DURATION MORE THAN 7 DAYS",
        points: [
          {
            title:
              "(21.1) If a vehicle is due for service during the booking period, we recommend the users to drop the vehicle for the servicing"
          },
          {
            title:
              "(21.2) We will not reimburse any costs for parts changed during servicing without our consent."
          }
        ]
      }
    ]
  })
};
</script>

