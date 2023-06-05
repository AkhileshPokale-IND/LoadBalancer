# Load Balancer

This repository contains a simple load balancer implementation in Go. It allows distributing incoming HTTP requests across multiple backend servers using a round-robin algorithm.

## Getting Started

To get started with the load balancer, follow the instructions below.

### Prerequisites

Make sure you have the following software installed on your system:

- Go (version 1.16 or higher)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/AkhileshPokale-IND/LoadBalancer.git
   ```
2. Change into the project directory:
   ```bash
   cd your-repository
   ```
3. Build the project:

   ```bash
   go build
   ```
### Usage

1. Edit the `main.go` file to specify the backend servers you want to load balance. Modify the `servers` slice in the `main` function to include the addresses of your backend servers:

   ```go
	   codeservers := []Server{
       newSimpleServer("http://backend1.com"),
       newSimpleServer("http://backend2.com"),
       newSimpleServer("http://backend3.com"),
   }
   ```
2. Run the load balancer:
   ```bash
   ./LoadBalancer
   ```

   The load balancer will start listening on the specified port (default is 8000).

3. Send HTTP requests to the load balancer:

   ``` bash
   curl http://localhost:8000
   ```

   The load balancer will distribute the requests among the backend servers.

### Configuration

You can customize the load balancer by modifying the following parameters:

- **Port**: The port on which the load balancer listens for incoming requests. Edit the `port` variable in the `NewLoadBalancer` function.
- **Load Balancing Algorithm**: The load balancer uses a round-robin algorithm by default. If you want to implement a different load balancing algorithm, you can modify the `getNexAvailableServer` method in the `LoadBalancer` struct.

### Contributing

Contributions to this repository are welcome! If you find any issues or want to add new features, feel free to submit a pull request.

### License

This project is licensed under the [MIT License](https://github.com/AkhileshPokale-IND/LoadBalancer/blob/main/LICENSE).

### Acknowledgments

This load balancer implementation is based on the examples provided in the Go standard library documentation.

## Contact

If you have any questions or suggestions, please feel free to open an issue or contact me at [akhilesh.pokale.edu@gmail.com](mailto:akhilesh.pokale.edu@gmail.com).

Enjoy using the load balancer!

