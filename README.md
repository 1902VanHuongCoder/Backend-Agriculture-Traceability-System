<h1 align="center">Agricultural Traceability System </h1> 
<img align="center" alt="Coding" src="https://github.com/user-attachments/assets/aba5355e-8a5d-4d8e-b3ca-b97a01eae1ef" />

# Explain project files 
- build/contracts: This folder contains Solidity codes that were compiled after run " truffle compile" command in CLI.
- contracts: This directory contains Solidity file.
- migrations: contains JS file to config which smart contracts will be compiled.
- traceability-frontend:  Front-end which use Smart Contracts (https://github.com/1902VanHuongCoder/Frontend_Agriculture_Traceability_System)
- truffle-config.js: Config file to connect to visual network on Ganache

# Project's images 
- Use metamask
![image](https://github.com/user-attachments/assets/a66aa2b1-5f50-4a40-85a1-835713f3dd53)
- Use Ganache
![image](https://github.com/user-attachments/assets/28a86347-e0b8-4785-bbf6-38f0cd0022ad)
- Tracing Page
  + Image 01:
    ![image](https://github.com/user-attachments/assets/9b3af6bf-7937-458b-9eb9-f75d4012d2db)
  + Image 02:
    ![image](https://github.com/user-attachments/assets/87fff25e-bde5-49ee-add3-37e5678cdee7)

# Agriculture_Traceability_System - Vietnamese Description
Hệ thống truy xuất nguồn gốc nông sản dựa trên blockchain là một ứng dụng hiện đại nhằm đảm bảo tính minh bạch và an toàn cho chuỗi cung ứng nông sản. Nền tảng Ethereum được sử dụng, với ngôn ngữ Solidity để phát triển các smart contract quản lý thông tin sản phẩm nông nghiệp. Người dùng có thể tương tác với blockchain thông qua Metamask, cho phép thực hiện giao dịch một cách an toàn.

Ganache mô phỏng mạng blockchain cục bộ, giúp kiểm tra và phát triển ứng dụng nhanh chóng mà không cần kết nối với mạng Ethereum thực tế. Giao diện người dùng được xây dựng bằng ReactJS, mang lại trải nghiệm mượt mà và tương tác nhanh chóng cho người dùng. TailwindCSS được áp dụng để tạo ra một giao diện hiện đại, dễ nhìn và thân thiện, giúp người tiêu dùng dễ dàng truy cập thông tin về nguồn gốc sản phẩm nông nghiệp.

Vite build tool giúp tối ưu hóa quá trình phát triển và xây dựng ứng dụng, nâng cao hiệu suất và giảm thời gian chờ. Hệ thống không chỉ giúp người tiêu dùng dễ dàng truy xuất nguồn gốc nông sản mà còn tạo ra một môi trường minh bạch, tăng cường sự tin tưởng giữa người tiêu dùng và nhà sản xuất, góp phần vào sự phát triển bền vững trong ngành nông nghiệp.

# Agriculture_Traceability_System - English Description
The "Agricultural Product Traceability System" leverages cutting-edge technologies to ensure transparency and accountability in the food supply chain. Built on the Ethereum blockchain, the system utilizes Solidity for smart contract development, enabling secure and tamper-proof records of agricultural products from farm to table. Users can interact with the blockchain through Metamask, a popular crypto wallet that facilitates seamless transactions and identity verification.

To create a robust development environment, Ganache is employed to simulate the Ethereum blockchain, allowing developers to test their smart contracts locally before deploying them on the mainnet. The front-end interface is crafted with ReactJS, providing a dynamic user experience, while TailwindCSS is integrated for responsive and visually appealing designs.

Using Vite as a build tool enhances performance and development speed, facilitating rapid iterations and a smooth workflow. This comprehensive system not only enhances consumer confidence by allowing them to trace the origins of their food products but also empowers farmers and producers by promoting ethical practices and transparency in agriculture. Overall, the Agricultural Product Traceability System exemplifies how modern technology can transform and innovate traditional supply chains.

# How to initialize blockchain project from start to end 
Để xây dựng một hệ thống truy xuất nguồn gốc nông sản dựa trên blockchain miễn phí sử dụng Ethereum, bạn có thể sử dụng các công nghệ phổ biến như Ethereum, Ganache, và Solidity. Hướng dẫn này sẽ bao gồm các bước chi tiết và các công cụ cần thiết cho việc phát triển dựa trên blockchain Ethereum.

1. Blockchain Layer (Ethereum và Smart Contract):
Ethereum: Nền tảng blockchain phi tập trung phổ biến nhất hiện nay, cho phép phát triển và triển khai các hợp đồng thông minh.
Solidity: Ngôn ngữ lập trình chính để viết hợp đồng thông minh trên Ethereum.
Ganache: Công cụ mô phỏng một blockchain Ethereum cục bộ, giúp bạn thử nghiệm và phát triển hợp đồng thông minh mà không cần phải triển khai lên mạng chính Ethereum.


2. Frontend Layer:
ReactJS: Giao diện người dùng động giúp quản lý dữ liệu từ blockchain và hiển thị chuỗi cung ứng sản phẩm.
Web3.js hoặc Ethers.js: Thư viện JavaScript để kết nối và tương tác với blockchain Ethereum từ frontend. Web3.js là phổ biến nhưng Ethers.js nhẹ hơn và dễ sử dụng hơn.
Truffle: Một framework giúp phát triển, compile, và triển khai hợp đồng thông minh một cách dễ dàng. Truffle cũng hỗ trợ tích hợp với Ganache để thử nghiệm cục bộ.

3. Quy trình Phát triển Hệ thống:
Bước 1: Cài đặt môi trường phát triển
Cài đặt Ganache: Ganache mô phỏng một blockchain Ethereum cục bộ với các tài khoản và giao dịch mẫu.
npm install -g ganache-cli

Chạy Ganache:
ganache-cli

Hoặc sử dụng ứng dụng Ganache với giao diện đồ họa từ Truffle.

Cài đặt Truffle: Truffle là một framework giúp bạn phát triển, kiểm thử và triển khai hợp đồng thông minh một cách dễ dàng.
npm install -g truffle

Khởi tạo dự án Truffle:
truffle init



Bước 2: Viết hợp đồng thông minh bằng Solidity
Trong thư mục contracts/, tạo file ProductTraceability.sol:
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract ProductTraceability {
    struct Farmer {
        string name;
        string location;
        string productDetails;
    }
    
    struct Transporter {
        string name;
        string licensePlate;
        uint timestamp;
    }
    
    struct Retailer {
        string name;
        string storeLocation;
        uint timestamp;
    }

    Farmer[] public farmers;
    Transporter[] public transporters;
    Retailer[] public retailers;

    function addFarmer(string memory name, string memory location, string memory productDetails) public {
        Farmer memory newFarmer = Farmer(name, location, productDetails);
        farmers.push(newFarmer);
    }

    function addTransporter(string memory name, string memory licensePlate, uint timestamp) public {
        Transporter memory newTransporter = Transporter(name, licensePlate, timestamp);
        transporters.push(newTransporter);
    }

    function addRetailer(string memory name, string memory storeLocation, uint timestamp) public {
        Retailer memory newRetailer = Retailer(name, storeLocation, timestamp);
        retailers.push(newRetailer);
    }

    function getFarmers() public view returns (Farmer[] memory) {
        return farmers;
    }

    function getTransporters() public view returns (Transporter[] memory) {
        return transporters;
    }

    function getRetailers() public view returns (Retailer[] memory) {
        return retailers;
    }
}

Compile hợp đồng thông minh:

truffle compile

Triển khai hợp đồng lên Ganache (mạng cục bộ): Trong thư mục migrations/, tạo file 2_deploy_contracts.js

const ProductTraceability = artifacts.require("ProductTraceability");

module.exports = function (deployer) {
  deployer.deploy(ProductTraceability);
};

Sau đó chạy lệnh triển khai:
truffle migrate --network development




Bước 3: Tạo giao diện người dùng với React và Ethers.js
Khởi tạo dự án React:

npx create-react-app traceability-frontend --template typescript
cd traceability-frontend

Cài đặt Ethers.js:
npm install ethers



Cài đặt thêm Bootstrap hoặc Material-UI để xây dựng giao diện.

Trong file App.tsx, bạn có thể kết nối và tương tác với hợp đồng thông minh:
import React, { useState, useEffect } from 'react';
import { ethers } from 'ethers';
import ProductTraceabilityABI from './ProductTraceabilityABI.json'; // ABI của hợp đồng

const App: React.FC = () => {
  const [farmers, setFarmers] = useState([]);

  useEffect(() => {
    const loadBlockchainData = async () => {
      const provider = new ethers.providers.Web3Provider((window as any).ethereum);
      const signer = provider.getSigner();
      const contractAddress = "0xYourContractAddress"; // Địa chỉ hợp đồng trên Ganache
      const contract = new ethers.Contract(contractAddress, ProductTraceabilityABI, signer);

      const farmersData = await contract.getFarmers();
      setFarmers(farmersData);
    };

    loadBlockchainData();
  }, []);

  return (
    <div>
      <h1>Farmers List</h1>
      <ul>
        {farmers.map((farmer: any, index) => (
          <li key={index}>
            {farmer.name} - {farmer.location}
          </li>
        ))}
      </ul>
    </div>
  );
};

export default App;



Bước 4: Kết nối MetaMask và thử nghiệm
MetaMask: Là ví tiền điện tử dùng để tương tác với Ethereum. Cài đặt MetaMask và cấu hình để kết nối với mạng Ganache.
Trong trình duyệt, MetaMask sẽ yêu cầu bạn xác nhận các giao dịch được gửi từ frontend tới hợp đồng thông minh.
4. Tính năng mở rộng
Mã QR: Bạn có thể tích hợp mã QR để người dùng cuối có thể quét và kiểm tra lịch sử chuỗi cung ứng sản phẩm.
Role-based Access Control: Thêm cơ chế phân quyền cho các vai trò khác nhau trong chuỗi cung ứng như nông dân, nhà vận chuyển, và nhà bán lẻ.
Chữ ký số: Để đảm bảo tính an toàn và xác thực thông tin.
5. Bảo mật
Sử dụng các kỹ thuật an toàn của Ethereum như mã hóa dữ liệu, cơ chế xác thực người dùng, và phân quyền để đảm bảo hệ thống không bị xâm nhập và thông tin không bị giả mạo.
Với các bước trên, bạn có thể xây dựng một hệ thống truy xuất nguồn gốc nông sản hoàn chỉnh sử dụng blockchain Ethereum, đảm bảo tính minh bạch và bảo mật thông tin.



