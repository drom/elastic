## Link protocol

All elastic components connected with links. Signaling on each link has to folow these rules:

### Rules

   * initiator agent drives `req` and `dat` signals
   * target agent drives `ack` signal
   * `req & ack` @(posedge clk) = single transaction
   * once initiator asserted `req`, both `req` and `dat` has to stay unchanged until target acknowledge it with `ack`.
