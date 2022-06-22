# Notification Capability

## Diagram

![NotificationCapability](../../assets/Notification-Capability.png)


## Description

The Notification Capability is responsible for queuing and deliverying notifications to the user.  This could include in-app or out-of-band (email).

Note that the Event Queue is a critical part of this app as it guarentees "eventual delivery" and ensures notifications aren't delivered multiple places. i.e. if you view "notifications" in the UI before the email trigger happens, the event will be queued and you won't get a duplicate email notification.
## Use Cases

* Scheduling notifications
* Deliverying notifications via app
* Delviering notifications via email
* Managing state of notifications (read, unread, done, etc.)

## Components

* Notification Capability Service: Primary logic used by routes and other microservices.
* Event Queue: Event-driven bus for queuing notifications.
* Email Service: Some cron-like service that looks for notifications (that support email delivery) and sends them if they exist in the queue.
* Persistent Storage Capability: This capability is used by the Notification Capability Service to store notifications that have been "seen" and don't need to be "queued" but should exist for the user.

## Architectural Characteristics
* Eventual Delivery

## ADR
- [NotifyQueues](../../ADRs/NotifyQueues.md)
- [NotifyUsePersistenceCap](../../ADRs/NotifyUsePersistenceCap.md)
