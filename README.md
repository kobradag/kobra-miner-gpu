# kobra-miner-gpu

A Kobra high performance CPU miner

USAGE:
    kobra-miner [OPTIONS] --mining-address <MINING_ADDRESS>

OPTIONS:
    -a, --mining-address <MINING_ADDRESS>
            The Kobra address for the miner reward

        --cuda-device <CUDA_DEVICE>
            Which CUDA GPUs to use [default: all]

        --cuda-disable
            Disable cuda workers

        --cuda-no-blocking-sync
            Actively wait for GPU result. Increases CPU usage, but removes delays that might result in red blocks. Can have lower workload.

        --cuda-nonce-gen <CUDA_NONCE_GEN>
            The random method used to generate nonces. Options: (i) xoshiro - each thread in GPU will have its own random state, creating a (pseudo-)independent xoshiro sequence (ii) lean - each GPU will have a single random nonce, and each GPU thread will work on nonce + thread id.

            [default: lean]

        --cuda-workload <CUDA_WORKLOAD>
            Ratio of nonces to GPU possible parrallel run [default: 64]

        --cuda-workload-absolute
            The values given by workload are not ratio, but absolute number of nonces [default: false]

    -d, --debug
            Enable debug logging level

    -h, --help
            Print help information

        --mine-when-not-synced
            Mine even when kobra says it is not synced, only useful when passing `--allow-submit-block-when-not-synced` to kobra  [default: false]

    -p, --port <PORT>
            Kobrad port [default: Mainnet = 44448, Testnet = 44450]

    -s, --kobra-address <KOBRA_ADDRESS>
            The IP of the kobra instance

            [default: 127.0.0.1]

    -t, --threads <NUM_THREADS>
            Amount of CPU miner threads to launch [default: 0]

        --testnet
            Use testnet instead of mainnet [default: false]

    -V, --version
            Print version information
