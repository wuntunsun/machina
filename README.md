# Machina

To both modernise my C++ and get further insight into machine learning (ML), I am following a course in ML for C++.
https://www.udemy.com/course/machine-learning-in-cpp/

The course code uses new and many C constructs I have chosen to avoid.

The k-nearest neighbours (KNN) algorithm is a simple, supervised machine learning algorithm that can solve classification and regression problems. 

## The Data class template

This example uses the http://yann.lecun.com/exdb/mnist/ dataset.

The Data template class allows for 'readings' of the IDX format housed in std::array rather than std::vector for performance. Promoting the dimension of the std::array to be a template parameter allows for the typesafe implementation of methods that require two arguments of equal size, e.g. 'calculate_euclidian_distance'.

It offers static factory methods that return std::unique_ptr for improved memory management compared to naked pointers and new.

## Performance

I experimented with 'discover_best_k_value' and 'validate' over the entire training set, but the execution time is, as expected, prohibitively long. 

Other toolkits apply structures to the dataset that accelerate operation.
https://towardsdatascience.com/make-knn-300-times-faster-than-scikit-learns-in-20-lines-5e29d74e76bb

