# centramart-system
It is an ongoing backend-focused project to design a single-vendor e-commerce system where inventory is distributed across multiple physical branches and a single order can be fulfilled by more than one location.
The goal of this project is to understand real-world system design problems seen in large retail platforms (branch-level inventory, order orchestration, COD handling, VAT locking), not to quickly build a demo app.
#What problem this explores

  ##Most basic e-commerce systems assume:
  -centralized inventory
  -one order = one shipment
  -That breaks down when inventory lives in different branches.
  -This project explicitly models:
  -branch-owned inventory
  -order vs fulfillment separation
  -multi-branch fulfillment for a single order
  
#Key design decisions
  -Inventory is owned by branches, not globally
  -Orders are financial commitments (prices & VAT are locked at creation)
  -Fulfillment is branch-scoped and handled independently
  -One order can result in multiple fulfillments
  -Stock is reserved at order creation, deducted during fulfillment
  -COD and delivery failures release reserved stock correctly
#Current status
  -System abstraction and domain model defined
  -Module responsibilities documented
  -API contracts written (design-level)
  -Database schema planned
  -UI flows adapted from Figma community designs
