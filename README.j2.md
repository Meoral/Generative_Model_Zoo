# The Generative Model Zoo

Every week, new GAN,VAE papers are coming out and it's hard to keep track of them all,So, here's a list of what started as a fun activity compiling all named gans,vaes!

You can also check out the same data in a tabular format with functionality to filter by year or do a quick search by title [gan](https://github.com/tangzhenyu/Generative_Model_Zoo/blob/master/gans.tsv),[vae](https://github.com/tangzhenyu/Generative_Model_Zoo/blob/master/vae.tsv).

<p align="center"><img width="50%" src="cumulative_gans.jpg" /></p>
#### Generative Adversarial Nets (GAN)

{% for gan in gans %}
* {{ gan['Abbr.'] }} - [{{ gan['Title'] }}]({{ gan['Arxiv'] }})
  {%- if gan['Official_Code'] != '-' -%} 
  {#- #} ([github]({{ gan['Official_Code'] }}))
  {% else %} {# space removed if no github repository #}

  {% endif %}
{%- endfor %}

<p align="center"><img width="50%" src="cumulative_vaes.jpg" /></p>

#### Variational Autoencoder (VAE)

{% for vae in vaes %}
* {{ vae['Abbr.'] }} - [{{ vae['Title'] }}]({{ vae['Arxiv'] }})
  {%- if vae['Official_Code'] != '-' -%} 
    {#- #} ([github]({{ vae['Official_Code'] }}))
	  {% else %} {# space removed if no github repository #}

	    {% endif %}
		{%- endfor %}

#### Restricted Boltzmann Machine (RBM)
* [Binary RBM with Contrastive Divergence](http://www.cs.toronto.edu/~fritz/absps/cdmiguel.pdf)
* [Binary RBM with Persistent Contrastive Divergence](http://www.cs.toronto.edu/~tijmen/pcd/pcd.pdf)

## Dependencies

1. Install miniconda <http://conda.pydata.org/miniconda.html>
2. Do `conda env create`
3. Enter the env `source activate generative-models`
4. Install [Tensorflow](https://www.tensorflow.org/get_started/os_setup)
5. Install [Pytorch](https://github.com/pytorch/pytorch#installation)
