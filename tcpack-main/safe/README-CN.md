# safetcpack

safetcpack is a thread-safe version of tcpack.

Differences from tcpack

Unlike tcpack, safetcpack allows you to create multiple packers for a single TCP connection and use them concurrently across multiple goroutines.

Note: Concurrently using multiple packers on the same TCP connection may result in messages being sent and received in an unpredictable order. If you need to guarantee message ordering, use tcpack and avoid concurrent access.