# Performance Testing of Flex App with JMeter

## 📱 Project Overview

This repository contains comprehensive load and performance testing documentation for **FlexEm**, a social currency application built on a flexible platform. The project includes JMeter test plans, test data, and detailed performance analysis reports for validating the application's behavior under various load conditions.

FlexEm is designed as a creator-first application that partners with renowned brands across diverse industries to deliver a seamless user experience with modern visuals.

## 📊 Test Scenarios

This project includes performance testing for the following user-based scenarios:

### Registration Tests
- **350 User Registration Success (60 min)**
- **500 User Registration Success (60 min)**
- **1000 User Registration Success Fresh DB (60 min)**
- **1000 User Registration with Existing Email Failure (60 min)**
- **600 User Registration with Existing Email Failure (60 min)**
- **800 User Registration with Existing Email Failure (60 min)**
- **15,000 User Registration** (Large scale test)

### Login Tests
- **1000 User Login Success (60 min)**

### Brands & Offers Tests
- **1000 User Brands By Category, Brands, Offers Success (60 min)**
- **1000 User Brands By Category, Brands, Offers, Claim Create Success (60 min)**
- **900 User Brands By Category, Brands, Offers, Claim Create Success (60 min)**
- **900 User Brands By Category, Brands, Offers, Claim Create, Get Claim Failure (60 min)**
- **800 User Brands By Category, Brands, Offers, Claim Create, Get Claim Success (60 min)**

## 📁 Repository Structure

```
Performance-Testing-of-Flex-App-with-Jmeter/
├── FlexEm Test Plan.jmx                    # Main JMeter test plan file
├── FlexEm Load Test Report.pdf             # Detailed performance analysis report
├── FlexEm_Login - Sheet(1000 user) - Sheet1.csv           # Login test data
├── FlexEm_Registration - Sheet(1000 user) - Sheet1.csv    # Registration test data
├── FlexEm_15000_users - FlexEm_15000_users.csv.csv        # Large scale test data
├── [Test Scenario Directories]/            # Individual test result directories
└── README.md                               # This file
```

## 🛠️ Tools & Technologies

- **JMeter**: Apache JMeter for load testing and performance analysis
- **Test Data**: CSV files containing user credentials and test data
- **Reporting**: Comprehensive PDF report with performance metrics

## 📈 Key Test Metrics

Each test scenario evaluates:
- **Response Times**: Average, minimum, and maximum response times
- **Throughput**: Requests per second under load
- **Error Rate**: Percentage of failed requests
- **Load Distribution**: User ramp-up and hold time
- **System Behavior**: Performance degradation patterns under stress

## 🚀 Getting Started

### Prerequisites
- Apache JMeter 5.0 or later
- Java Runtime Environment (JRE) 8 or higher
- CSV test data files
- Adequate system resources for load simulation

### Running Tests

1. **Open JMeter Test Plan**
   ```bash
   jmeter -n -t "FlexEm Test Plan.jmx" -l results.jtl
   ```

2. **Generate HTML Report**
   ```bash
   jmeter -n -t "FlexEm Test Plan.jmx" -l results.jtl -j jmeter.log -e -o report
   ```

3. **View Results**
   - Check the generated HTML report in the output directory
   - Review the `FlexEm Load Test Report.pdf` for detailed analysis

## 📝 Test Data Files

- **FlexEm_Login - Sheet(1000 user) - Sheet1.csv**: Contains 1000 user credentials for login tests
- **FlexEm_Registration - Sheet(1000 user) - Sheet1.csv**: Contains 1000 registration test data entries
- **FlexEm_15000_users - FlexEm_15000_users.csv.csv**: Contains 15,000 user records for large-scale testing

## 📊 Performance Report

The comprehensive **FlexEm Load Test Report.pdf** includes:
- Executive summary of test objectives and scope
- Detailed performance metrics for each test scenario
- Response time analysis and distribution
- Error analysis and failure patterns
- Recommendations for optimization
- Comparative analysis of different load levels

## 🎯 Testing Objectives

- Validate system stability under normal and peak loads
- Identify performance bottlenecks
- Determine system breaking points
- Assess scalability of the FlexEm application
- Validate error handling under high load conditions
- Ensure consistent user experience across different load scenarios

## 💡 Key Findings

Performance testing was conducted with varying user loads (350 to 15,000 concurrent users) over 60-minute intervals to understand system behavior under different stress conditions. The tests covered critical user journeys including registration, login, and brand/offers browsing functionality.

## 📋 Test Coverage

- ✅ Successful user flows (registration, login, brand browsing)
- ✅ Error scenarios (duplicate email registration)
- ✅ Complex multi-step workflows (brand navigation with claim creation)
- ✅ Large-scale user load simulation (15,000 users)
- ✅ Various concurrent user levels for trend analysis

## 🔧 Customization

To customize tests:

1. Modify the JMeter test plan (`FlexEm Test Plan.jmx`) to adjust:
   - User count (Thread Group settings)
   - Ramp-up time
   - Hold time/duration
   - Target endpoints
   - Think time between requests

2. Update CSV data files with your test data

3. Run tests against your target environment

## 📞 Support & Documentation

For more information about the test scenarios and results, refer to:
- `FlexEm Load Test Report.pdf` - Comprehensive test report
- JMeter documentation: https://jmeter.apache.org/
- Individual test scenario folders for detailed results

## 📅 Project Timeline

- **Repository Created**: July 1, 2025

## 📈 Performance Testing Best Practices

- Conduct tests in a dedicated staging environment
- Monitor system resources during test execution
- Analyze results to identify optimization opportunities
- Document findings and recommendations
- Plan capacity based on projected growth
- Conduct regular regression tests

## ⚠️ Important Notes

- Tests should be run in a controlled environment to avoid impact on production systems
- Ensure database is properly prepared before running registration tests
- Monitor server resources during large-scale tests (15,000 users)
- Review error logs alongside test reports for comprehensive analysis

