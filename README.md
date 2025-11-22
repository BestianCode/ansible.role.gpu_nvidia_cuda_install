# NVIDIA GPU + CUDA Install Role

Minimal role to prep Ubuntu 24.04 (x86_64) GPU nodes with the NVIDIA open server driver stack, CUDA toolkit, container runtime, and RDMA tooling.

## Installation

Install from Ansible Galaxy (preferred):

```bash
ansible-galaxy role install bestiancode.gpu_nvidia_cuda_install
```

Or pull straight from GitHub:

```bash
ansible-galaxy role install git+https://github.com/BestianCode/ansible.role.gpu_nvidia_cuda_install.git
```

Sample `requirements.yml` entry:

```yaml
roles:
  - name: bestiancode.gpu_nvidia_cuda_install
```

## Usage

Minimal playbook:

```yaml
- hosts:
    - gpu_nodes
  become: true
  roles:
    - role: bestiancode.gpu_nvidia_cuda_install
      vars:
        nvidia_install_fabric_manager: true
        nvidia_test_gpu_in_container: true
```

## Links

- **GitHub**: <https://github.com/BestianCode/ansible.role.gpu_nvidia_cuda_install>
- **Galaxy**: <https://galaxy.ansible.com/ui/standalone/roles/BestianCode/gpu_nvidia_cuda_install>
