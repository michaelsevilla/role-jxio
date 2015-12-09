============================================
role-jxio: module for building/deploying JXIO
============================================

This is a role module that plugs into the UC Santa Cruz System Research Lab's (SRL's) [infra](https://github.com/systemslab/infra) reproducibility framework. For more information, please see that git repository. This role module has a [Docker](https://www.docker.com/enterprise) image for running [JXIO](https://github.com/accelio/JXIO) and the [Ansible](http://www.ansible.com) "role" scripts for deploying it. 

Install
=======
This should be overlayed over the [infra](https://github.com/systemslab/infra)

1. Setup the reproducibility framework:

```bash
git clone --recursive https://github.com/systemslab/infra
```

2. Overlay this code onto ``infra``:

```bash
cd infra/roles/
git clone https://github.com/michaelsevilla/role-jxio.git 
```

3. Move the experiment to the ``infra`` experiment folder:

```bash
cp jxio.yml ../experiments/jxio.yml
```

4. Launch the emaster and start the experiment:

```bash
cd ../bin
./emaster.sh
```

