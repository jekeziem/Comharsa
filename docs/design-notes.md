# design notes

What each part of Comharsa is for, and the behaviour it's designed around.

## 1. the room finds you

**The situation.** During Storm Éowyn, the official advice was to check ESB's online outage map. That needs power and a signal, the two things people didn't have.

**The design.** Comharsa doesn't wait to be opened. When the network drops, phones nearby find each other over Bluetooth and the street gets a room, named after the street. Messages hop from phone to phone, so the house at the far end can still reach the house at the other.

**Open question.** iPhones heavily limit what an app can do over Bluetooth while it's closed. A real version may need people to open it when a red warning is issued, before the power goes.

## 2. built for milling

**The behaviour.** When people receive a warning, they rarely act on it straight away. They look for confirmation first: they ask others, look outside, check another source. Warning researchers call this *milling*.

**The design.** Every update carries a confirmation count. "Tree down at the top of the road" shows how many neighbours have seen it, and only reads as confirmed once three have. Anyone can also say "not sure". The point isn't to stop people milling, it's to make milling fast.

## 3. the bystander effect

**The behaviour.** The more people who could help, the less responsible each one feels (Latané & Darley). On a street of twenty houses, everyone assumes someone else has checked on the woman at no. 14.

**The design.** Check-ins are three buttons: *i'm ok*, *need help*, *can help*. The room says out loud who hasn't been heard from yet. Once a name is on the screen, checking on them is somebody's job, not everybody's.

## 4. safety first

**The risk.** A live map of who's home during a storm is also a map of who's alone, who's elderly, and which houses are empty. In the wrong hands, it's a target list.

**The design.**
- only phones in the room can see the map
- anyone can hide their own house
- the room, its messages and the map delete themselves 24 hours after the power comes back
- there's no account, so there's nothing to hand over afterwards

## what the prototype simulates

The street, the six neighbours and their messages are scripted. Everything else (the check-ins, the confirmations, the map, hiding your house, the room closing when the power returns) works as designed.
