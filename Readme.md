# Single Cell on Colab

![Allen Institute's Cell Diversity pre-built tSNE](http://reconstrue.com/projects/single_cell_on_colab/demo/aibs_cell_diversity_pre_tsned_by_datashader.png)


The goal of this project is to optimize [Google
Colab](https://colab.research.google.com/) for the purpose of
performing single cell analysis.

Initially the project is integrating existing popular tools in both
Python and R.  The longer term goal is to build out a set of
components which can be assembled into end-to-end GPU pipelines. In
such a pipeline, the data would be downloaded and parked on the GPU
wherein all analysis computation would happen. Apache Arrow enables such architectures, as
illustrated in the following diagram from Nvidia:

<img src="https://github.com/rapidsai/cudf/raw/branch-0.12/img/rapids_arrow.png" width="600px" />

For the context of single cell analysis, the types of GPU powered
compenents being assembled include:

- Data parsers (e.g. [nvParse](https://github.com/antonmks/nvParse) for CSV, sparse coordinate matrices, etc.)
- [Multi-GPU PCA](https://github.com/rapidsai/cuml/issues/68)
- [GPGPU Linear Complexity t-SNE Optimization](https://biovault.github.io/nptsne/)
- [UMAP on RAPIDS (15x Speedup)vv](https://medium.com/the-artificial-impostor/umap-on-rapids-15x-speedup-f4eabfbdd978)
- [cuDatashader](https://github.com/rapidsai/cuDataShader): Datashader implemented on GPU by Rapids

## Related notebooks in other repos

- [allensdk_on_colab.ipynb](https://github.com/reconstrue/neuro_on_colab/blob/master/platform/allensdk_on_colab.ipynb): install and debug AllenSDK on Colab
- [colab_vm_config.ipynb](https://github.com/reconstrue/neuro_on_colab/blob/master/platform/colab_vm_config.ipynb): stats on the VM 
- [git_console.ipynb](https://github.com/reconstrue/neuro_on_colab/blob/master/platform/git_console.ipynb): manually git on Colab
- [python_using_r.ipynb](https://github.com/reconstrue/neuro_on_colab/blob/master/platform/python_using_r.ipynb)


## Presentation

### Seattle Cell Science Symposium 2019

The first public presentation was at [Seattle Cell Science Symposium 2019](https://alleninstitute.org/media/filer_public/19/80/19801df8-8001-45ea-bcf9-a731281d98a3/2019_cellsciencesymp_flyer.pdf)

#### Lightening talk slide

<table><tr><td>
  <img src="http://reconstrue.com/projects/single_cell_on_colab/presentations/seattle_cell_lightening_slide.png"/>
</td></tr></table>

#### Poster
<table><tr><td>
  <img src="http://reconstrue.com/projects/single_cell_on_colab/presentations/2019_12_seattle_cell_poster.png" /> 
</td></tr></table>

