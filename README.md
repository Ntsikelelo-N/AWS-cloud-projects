# End-to-End Data Engineering Project
## Overview

This project demonstrates how to build a full data engineering pipeline for analyzing trending YouTube videos. It covers ingestion of raw data, transformation and cleaning, storing in a data lake/warehouse architecture, and querying for insights. The project targets data engineers and data scientists looking to learn scalable data workflows using AWS services.

## Motivation

The YouTube trending dataset provides an opportunity to handle semi-structured JSON data from multiple regions.

The project focuses on teaching practical data engineering — ingestion, ETL, data lake, and analytics.

It highlights the importance of clean, reliable, and queryable data for downstream analytics or ML.

The use of AWS demonstrates production-grade, scalable pipelines.

## Scope & Objectives
### Scope

Included:

 - Downloading YouTube trending data (from Kaggle/YouTube API).

 - Uploading raw data into AWS S3 buckets.

 - Using AWS services: IAM, S3, Glue, Athena.

 - Cleaning JSON data, converting to Parquet, partitioning by region.

 - Querying for insights using Athena.

### Objectives

 - Build a YouTube data lake architecture with raw & cleaned zones.

 - Use AWS services to build a scalable ETL pipeline.

 - Transform semi-structured JSON into tabular Parquet files.

 - Enable regional and categorical trend analysis.

 - Deliver a reproducible, cloud-based data pipeline.

## Architecture / Design
### High-level Architecture

 - Raw Zone: S3 bucket for unprocessed files.

 - Cleansed Zone: Parquet files in another S3 bucket.

 - Metadata Layer: AWS Glue Data Catalog.

 - Query Layer: Athena SQL queries.

 - Transformation Layer: AWS Lambda or Glue jobs for ETL.

 - Security: IAM roles and permissions.

### Data Flow

 - Download trending data (e.g., US, IN, JP).

 - Upload to S3

 - Trigger AWS Glue or Lambda on upload.

 - Flatten and clean JSON, convert to Parquet.

 - Store cleaned data in s3://youtube/processed/

 - Query with Athena via Glue Catalog.

4.3 Technologies / Tools

 - Languages: Python (Lambda, Glue)

 - AWS Services: S3, IAM, Lambda, Glue, Athena

 - Data Formats: JSON, Parquet

 - Source: Kaggle YouTube Trending Dataset

## Implementation
### Setup & Installation

Prerequisites:

 - AWS Account and permissions.

 - AWS CLI installed and configured.
