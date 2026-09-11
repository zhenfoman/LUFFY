# LUFFY Development Repository

> 🚧 **Development Branch** - This is the main development repository for LUFFY (Learning to Reason Under Off‑Policy Guidance)

## About LUFFY

LUFFY is a reinforcement learning framework that bridges the gap between zero-RL and imitation learning by incorporating off-policy reasoning traces into the training process. This repository contains the core implementation and development work.

## 🔧 Development Status

This repository is under active development. Many features are currently being implemented or need refactoring.

## 🚀 Quick Start

⚠️ **Note**: This development version has incomplete implementations. Many features are marked as TODO and need to be completed before production use.

```bash
# Clone the repository
git clone <repository-url>
cd LUFFY

# Install dependencies
pip install -r luffy/requirements.txt

# Note: Some functionality is incomplete - check TODO list below for details
```

## 📁 Repository Structure

```
LUFFY/
├── luffy/                 # Core framework
│   ├── deepscaler/        # Scaling utilities (⚠️ API integration needed)
│   ├── verl/              # RL training components (⚠️ Some features incomplete)
│   └── ...
├── data/                  # Training data and scripts
├── eval_scripts/          # Evaluation utilities
├── exp_scripts/           # Experiment scripts
└── README.md              # This file
```

## ⚠️ Development Notes

- This is a **development version** with incomplete implementations
- Many functions contain TODO markers indicating pending work
- API integrations (OpenAI, Gemini) are currently placeholder implementations
- FSDP and distributed training features need completion


### 🔴 High Priority TODOs

- **API Integration**: ~~OpenAI~~ ✅ OpenAI core implemented; Gemini API implementation still needed
- **Reward System**: Parallel processing and validation for reward computation  
- **FSDP Training**: Model loading and distributed training setup
- **Data Processing**: ~~Batch dimension operations~~ ✅ fold/unfold batch dim implemented; optimization TODOs remain

### 📝 Complete TODO List

- [x] **luffy/deepscaler/utils.py:45** - Implement OpenAI API client initialization ✅
- [x] **luffy/deepscaler/utils.py:46** - Add proper authentication handling ✅
- [x] **luffy/deepscaler/utils.py:47** - Implement exponential backoff retry logic for rate limits ✅
- [x] **luffy/deepscaler/utils.py:48** - Add comprehensive error handling for different API errors ✅
- [x] **luffy/deepscaler/utils.py:49** - Implement response parsing and validation ✅
- [ ] **luffy/deepscaler/utils.py:50** - Add logging for API calls and errors
- [ ] **luffy/deepscaler/utils.py:51** - Support batch processing for multiple prompts
- [ ] **luffy/deepscaler/utils.py:52** - Add timeout configuration for API calls
- [ ] **luffy/deepscaler/utils.py:88** - Implement Vertex AI initialization and authentication
- [ ] **luffy/deepscaler/utils.py:89** - Configure safety settings for content generation
- [ ] **luffy/deepscaler/utils.py:90** - Set up GenerativeModel with proper system instructions
- [ ] **luffy/deepscaler/utils.py:91** - Implement retry logic with exponential backoff
- [ ] **luffy/deepscaler/utils.py:92** - Add comprehensive error handling for API access issues
- [ ] **luffy/deepscaler/utils.py:93** - Handle rate limiting and quota management
- [ ] **luffy/deepscaler/utils.py:94** - Implement response validation and text extraction
- [ ] **luffy/deepscaler/utils.py:95** - Add support for different generation configurations
- [ ] **luffy/test.py:1590** - add smaller page sizes when https://github.com/Dao-AILab/flash-attention/pull/824 is merged
- [ ] **luffy/verl/examples/split_placement/split_monkey_patch.py:141** - make a canonical logger that supports various backend
- [ ] **luffy/verl/tests/e2e/check_results.py:21** - this function needs error handling
- [ ] **luffy/verl/tests/model/test_transformer.py:22** - (sgm): add more models for test
- [ ] **luffy/verl/tests/model/test_transformer.py:50** - (sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/model/test_transformer.py:111** - (sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/model/test_transformers_ulysses.py:34** - (sgm): add more models for test
- [ ] **luffy/verl/tests/model/test_transformers_ulysses.py:81** - (sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/model/test_transformers_ulysses.py:159** - (sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/ray/test_high_level_scheduling_api.py:25** - pass *args and **kwargs is bug prone and not very convincing
- [ ] **luffy/verl/tests/ray/test_worker_group_basics.py:43** - pass *args and **kwargs is bug prone and not very convincing
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:54** - (sgm): support FSDP hybrid shard for larger model
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:83** - it seems that manual offload is slowly than FSDP offload
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:123** - (zhangchi.usc1992): 1.